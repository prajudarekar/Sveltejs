<script>
import { createEventDispatcher } from "svelte";
let dispatcher=createEventDispatcher();
function checkinner(){
dispatcher("greet","hi,welcome")
}
</script>

<div>
    <button on:click={checkinner}>p Greet</button>
</div>