<script>
    import TabA from "./TabA.svelte";
    import TabB from "./TabB.svelte";
    import TabC from "./TabC.svelte";
    let activetab=TabA;
</script>

<div>
   <button on:click={()=>(activetab = TabA)} >t A</button>
   <button on:click={()=>(activetab== TabB)} >t B</button>
   <button on:click={()=>(activetab== TabC)} >t C</button>

   <svelte:component this={activetab}/>

</div>