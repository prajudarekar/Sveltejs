
<script>
  import Container from "./Container.svelte";
  import Header from "./Header.svelte";
  import Button from './Button.svelte';
  let showheader=false;

  let buttons=[
    {value:0,text:"ummmmmm"},
    {value:2,text:"i sure do"},
    {value:-1,text:"gross"},

  ];
  let score=0;
</script>

{#if showheader}
<Header/>
{/if}
<Container>
 <p> what do you like pizza? Score {score}</p>
  <Button  {buttons} on:click={(e)=>score+=e.detail.value}/>
  <button on:click={()=>showheader=true}>Click me</button>
</Container>

<style>
  
</style>
