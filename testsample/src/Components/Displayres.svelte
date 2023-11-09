<script>
    import Mybar from "./Mybar.svelte";
    import Mychart from "./Mychart.svelte";
  import Mydonut from "./Mydonut.svelte";
    import { mchart } from "./stores.js";
    
    let chart;
    mchart.subscribe(value=>{
        chart=value;
    })
</script>

 {#if chart===''}
<h1>..</h1>
{:else}
{#if chart=== "pie"}
<Mychart/>
{/if}

{#if chart=== "bar"}
<Mybar/>
{/if}
{#if chart==="donut"}
<Mydonut/>
{/if}
<br>
 {/if}

