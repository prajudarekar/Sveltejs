<script>
import { mchart } from "./stores.js";
  import Mybar from "./Mybar.svelte";
  import Mydonut from "./Mydonut.svelte";
  import Mypie from "./Mypie.svelte";  
let chart;
mchart.subscribe(value=>{
    chart=value;
})
</script>

{#if chart===''}
<h1>..</h1>
{:else}
{#if chart=== "pie"}
<Mypie/>
{/if}

{#if chart=== "bar"}
<Mybar/>
{/if}
{#if chart==="donut"}
<Mydonut/>
{/if}
<br>
{/if}

