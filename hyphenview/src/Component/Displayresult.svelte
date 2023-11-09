<script>
    import { mchart } from "../stores.js";
    import Mybar from "../ChartComponents/Mybar.svelte";
    import Mydonut from "../ChartComponents/Mydonut.svelte";
    import Mypie from "../ChartComponents/Mypie.svelte";
  
    let chart;
    mchart.subscribe(value=>{
        chart=value;
    })
    </script>
    
    {#if chart===''}
...
    {:else}
    {#if chart=== "pie"}
    <div class="cardpie">
    <Mypie/>
    </div>
    {/if}
    
    {#if chart=== "bar"}
    <div class="card">
    <Mybar/>
    </div>
    {/if}
    {#if chart==="donut"}
    <div class="card">
    <Mydonut/>
    </div>
    {/if}
    <br>
    {/if}
    
    
<style>
   /* :global(svg ){
    position: absolute;
   left:25%;
    bottom: 55%;
    background: white;
    border:2px solid gainsboro;npm
  }*/
/*
:global(svg ) {
    position: absolute;
    top:25% !important;
    left:25%;
    
    background: white;
    border:2px solid red;
  }*/

</style>
    