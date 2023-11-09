<script>
    import {count} from '../store/stores.js'
        function handleDecrement(){
    count.update(value=>{
        return value-1
    })
        }
    </script>
    
    <button on:click={handleDecrement}>Decrement</button>