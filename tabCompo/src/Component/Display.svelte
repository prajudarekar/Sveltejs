<script>
    import {count} from "../store/stores.js";

let counter;

count.subscribe(value=>
    counter=value
)
</script>

<div>
    <h1>Current count {counter}</h1>
</div>