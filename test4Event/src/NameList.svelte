<script>
    let names=[
        {
            firstname:"Priya",
            lastname:"more"
        },
        {
            firstname:"Sonali",
            lastname:"kore"
        }
    ]
</script>

{#each names as name}
<slot name="hero" firstname={name.firstname} lastname={name.lastname} />
{/each}