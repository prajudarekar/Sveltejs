
<script>
    import {onMount} from 'svelte';
    let refvar;
    onMount(()=>{
        refvar.focus();
    })
</script>
<input class="form-control" type="text" bind:this={refvar}/>