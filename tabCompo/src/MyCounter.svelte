
<script context="module">

let totalcount=0;

export function getTotalcount(){
    return totalcount
}
</script>
<script>
    let count=0;
    function checkcount(){
        count=count+1;
        totalcount+=1;
    }
</script>

<div>
    <h1>{count}</h1>
    <button on:click={checkcount}>Increment</button>
</div>