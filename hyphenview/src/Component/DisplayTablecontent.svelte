<script>
    import { tablename } from "../stores.js";
      import Mytable1 from "../TableComponents/Mytable1.svelte";
    import Mytable2 from "../TableComponents/Mytable2.svelte";
    import Mytable3 from "../TableComponents/Mytable3.svelte";
    import Mytable4 from "../TableComponents/Mytable4.svelte";
    let name;
    tablename.subscribe(value=>{
        name=value;
    })
    </script>
    
    
    {#if name===''}
    <h1>..</h1>
    {:else}
    {#if name=== "tablenormal"}
    <div>
    <Mytable1/>
    </div>
    {/if}
    
    {#if name=== "tabledarkheaderanborder"}
    <div>
    <Mytable2/>
    </div>
    {/if}
    {#if name==="tabledarkhead"}
    <div>
    <Mytable3/>
    </div>
    {/if}
    {#if name==="tabledark"}
    <div>
    <Mytable4/>
    </div>
    {/if}
    <br>
    {/if}
    
<style>
  .card{
    margin:12%;
    width:340px;
    background-color: white;
    border:1px solid gainsboro;
  }
 
</style>
    
    