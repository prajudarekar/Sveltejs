<script>
      import {onMount} from "svelte";  

      let result=[];
    onMount(async()=>{
        const res=await fetch("http://localhost:3000/data");
        result=await res.json();
        
    });
</script>

<div>
    <h1>Api data</h1>
    {#each result as rs}

    <h1>{rs.rs1}</h1>
    <h1>{rs.rs2}</h1>
    <h1>{rs.rs3}</h1>


    {/each}
</div>