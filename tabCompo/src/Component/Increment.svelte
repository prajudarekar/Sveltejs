<script>
import {count} from '../store/stores.js'
    function handleincrement(){
count.update(value=>{
    return value+1
})
    }
</script>

<button on:click={handleincrement}>Increment</button>