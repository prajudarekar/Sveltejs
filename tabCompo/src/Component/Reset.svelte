<script>

    import {count} from '../store/stores.js'

    function checkReset()
    {
        count.set(0);
    }
</script>

<button on:click={checkReset}>Reset</button>