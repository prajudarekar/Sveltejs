<script>
    import {onMount} from 'svelte';
    
let post=[];
let pp;
let hk;

let test;
onMount(async()=>{
    const res=await fetch("https://jsonplaceholder.typicode.com/todos/");
post=await res.json();
})


</script>

<div>
    {#each post as posts(posts.id)}

    <h2>{posts.userId} {posts.title}  {posts.completed} </h2>

    <hr/>
    {:else}
    <p>Loading....</p>
    {/each}
</div>

<style>
    hr{
        color:red;
        size:25px;
    }
</style>