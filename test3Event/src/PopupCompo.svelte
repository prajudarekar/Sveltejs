
<script>
    import { createEventDispatcher } from "svelte";
    let dispatcher=createEventDispatcher();
</script>
<div>
    <h1>thsi popup Compo</h1>
    <button on:click={()=>dispatcher("close","vikas")}>Close popup</button>
</div>