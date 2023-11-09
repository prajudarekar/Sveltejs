
<script>
    import Face from './Face.svelte'
  import Container from './Container.svelte';
  import Header from './Header.svelte';
  let showheader=false;
  let say="true";
  setTimeout(()=>{
    showheader=true;
  },1000);
  </script>
   
  {#if showheader}
  <Header/>
  
  {/if}
  
  <Container>
  <main>
    <h1>Svelte Components</h1>
  <h4>gugygyu</h4>
  </main>
  {#if !say}
  <h1>Say:: Hiiiii......if</h1>
  {:else}
  don't say anything.............
  {/if}
  
  {#each [0,4,8] as items}
  <h1>item:: {items}</h1>
  {/each}
  
  
  <Face name="raj"/>
  </Container>
  <style>
  
  h1{
    color:red;
  }
  </style>
  