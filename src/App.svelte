<script>
  let todos = ['todo 1', 'todo 2', 'todo 3'];
  
  function autoAddTodo(){
    setTimeout(()=>{
      todos = [...todos, createRandomString()]
    }, 1000);
  }

  autoAddTodo()

  function createRandomString(){
    let text = (Math.random().toString(36).substring(7))
    return text
  }

  function addTodo(){
    todos = [...todos, createRandomString()]
  }
</script>

{#each todos as todo}
  <p>{todo}</p>
{/each}

<button on:click={addTodo}>add todo</button>
