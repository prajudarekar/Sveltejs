<script>
  import TabA from "./TabA.svelte";
  import TabB from "./TabB.svelte";
  import TabC from "./TabC.svelte";
  let activetab=TabA;
  import MyCounter,{getTotalcount} from "./MyCounter.svelte";
  import Display from "./Component/Display.svelte";
  import Increment from "./Component/Increment.svelte";
  import Decrement from "./Component/Decrement.svelte";
  import Reset from "./Component/Reset.svelte";
</script>


<div>
<Display/>
<Increment/>
<Decrement/>
<Reset/>
  <hr>
  <hr>
  <button on:click={()=>alert(getTotalcount())} >total count value </button>
  <h2>{getTotalcount()}</h2>
<MyCounter/>
<hr>
<MyCounter/>
<hr>
<MyCounter/>
<hr>
  <button on:click={()=>{activetab = TabA}}>Tab A</button>
  <button on:click={()=>(activetab = TabB)}>Tab B</button>
  <button on:click={()=>(activetab = TabC)}>Tab C</button>
  <svelte:component this={activetab}></svelte:component>
<!--{#if activetab == "TabA"}
<TabA />
{/if}
{#if activetab == "TabB"}
<TabB />
{/if}
{#if activetab == "TabC"}
<TabC />
{/if}-->
</div>