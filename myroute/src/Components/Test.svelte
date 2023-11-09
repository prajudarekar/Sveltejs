<script>
        import {onMount} from 'svelte';
    let result=[];
    onMount(async()=>{
    const res=await fetch('https://dummyjson.com/auth/login', {
  method: 'POST',
  headers: { 'Content-Type': 'application/json' },
  body: JSON.stringify({
    
    username: 'kminchelle',
    password: '0lelplR',
   // password:'rftfxrsdt',
    // expiresInMins: 60, // optional
  })
});
        result=await res.json();
        console.log(result);
    })

  
</script>


<div>
    <h1>{result.email}</h1>
    
</div>