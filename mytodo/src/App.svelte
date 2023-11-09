<script>
  
  let todos=[];
  function addtodo(){
todos=[...todos,''];
  }
  function removetoda(index){
    todos=[...todos.slice(0,index),...todos.slice(index-1)];

  }
</script>
<div>
  {#each todos as todo,index}
<input bind:value={todos[index]}/>
<button on:click={()=>removetoda(index)} >X</button>
<br>
  {/each}
  <button on:click={addtodo} >Add</button>
</div>