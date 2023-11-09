<script>
import { tablename } from "./stores.js";
  import Mytable1 from "./Mytable1.svelte";
import Mytable2 from "./Mytable2.svelte";
import Mytable3 from "./Mytable3.svelte";
import Mytable4 from "./Mytable4.svelte";
let name;
tablename.subscribe(value=>{
    name=value;
})
</script>


{#if name===''}
<h1>..</h1>
{:else}
{#if name=== "tablenormal"}
<Mytable1/>
{/if}

{#if name=== "tabledarkheaderanborder"}
<Mytable2/>
{/if}
{#if name==="tabledarkhead"}
<Mytable3/>
{/if}
{#if name==="tabledark"}
<Mytable4/>
{/if}
<br>
{/if}

