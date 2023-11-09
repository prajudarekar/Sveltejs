<script>
import {getContext} from 'svelte';
let pgender=getContext('gender-context');
</script>

<div>
    <h1>Compo B</h1>
    <h2>{pgender}</h2>
    <hr>
</div>