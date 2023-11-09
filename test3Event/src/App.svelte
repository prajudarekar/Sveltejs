<script>
  import CompoB from './CompoB.svelte';
  import Compoa from './Compoa.svelte';

import {setContext} from 'svelte';

  let gender="female";
setContext('gender-context',gender);
  let count=0;
  $: fullname="sagar more";
  function checkhandler(event,size){
    count=(count + size)
  }
  let formval={
name:'kjkk',
profiles:'',
country:'',
jobloc:'',
remotework:false,
skillval:[],
yearExp:''

  }
  function submitForm(event){
    event.preventDefault();
    console.log("formval:: "+formval);
  }

  let cc={
    fname:"rau",
    fcity:"pune"
  };

  import PopupCompo from './PopupCompo.svelte';
  let showpopup=false;

  function closecheck(event)
  {
    showpopup = false
    console.log("name after close:: "+event.detail);
    }
</script>

<div>
  
<button on:click={()=>{showpopup = true}}>Show Popup </button>

{#if showpopup}
<!--<PopupCompo on:close={()=>{showpopup = false}} />-->
  
<PopupCompo on:close={closecheck} />
{/if}

  <CompoB />
  <Compoa fcity="gg"/>
  <Compoa {...cc}/>

  <h1>{fullname}</h1>
  <button on:click={()=>count=count+1}>Click {count}</button>
  <button on:click={(event)=>checkhandler(event,10)}>click 2 {count}</button>

<p>{JSON.stringify(formval,null,2)}</p>
  <form on:submit={submitForm}>
    <label>Name</label>
    <input type="text" bind:value={formval.name}/>

    <label>Profile Summary</label>
    <textarea id ="profile" bind:value={formval.profiles}/>

    <label>Country</label>
    <select id="country" bind:value={formval.country}>
      <option value="">select any</option>
      <option value="pune">Pune</option>
      <option value="delhi" >Delhi</option>
    </select>

    <label>Job Location</label>
    <select id="jobloc" bind:value={formval.jobloc} multiple>
      <option value="">select any</option>
      <option value="pune">Pune</option>
      <option value="delhi" >Delhi</option>
      <option value="mumbai">Mumbai</option>
    </select>

    <input type="checkbox" id="remote-work" bind:checked={formval.remotework}/>
    <label>Remote Work</label>


    <label>Skill Set</label>
    <input type="checkbox"  id="html" value="html" bind:group={formval.skillval}>
    <label>HTML</label>
    <input type="checkbox"  id="css" value="CSS" bind:group={formval.skillval}>
    <label>css</label>
    <input type="checkbox"  id="javascript" value="javascript" bind:group={formval.skillval}>
    <label>javascript</label>
    

    
    <label>Experience Set</label>
    <input type="radio"  id="1year" value="1year" bind:group={formval.yearExp}>
    <label>1year</label>
    <input type="radio"  id="2year" value="2year" bind:group={formval.yearExp}>
    <label>2year</label>
    <input type="radio"  id="4year" value="4year" bind:group={formval.yearExp}>
    <label>4year</label>
    <button type="submit">Submit</button>
  </form>
</div>


<style>
  input + label{
    display: inline-flex;
  }
</style>