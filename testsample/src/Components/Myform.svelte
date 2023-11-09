<script>
    import Displayres from "./Displayres.svelte";
     import { mchart } from "./stores.js";
     let formval={
         cchart:'',
     }
   
 function mysubmit(){
   mchart.update(value=>{
     return value="pie";
 })
 }
 </script>
<div class="myform">
    <form >
        <p>Please select your favorite Web language:</p>
        <input type="radio" id="html" name="fav_language" value="HTML">
        <label for="html">HTML</label><br>
        <input type="radio" id="css" name="fav_language" value="CSS">
        <label for="css">CSS</label><br>
        <input type="radio" id="javascript" name="fav_language" value="JavaScript">
        <label for="javascript">JavaScript</label>
      
        <br>  
      
        <input type="submit" value="Submit" on:click={mysubmit}>
      </form>
      
</div>

<style>
    .myform{
        width:600px;
        height:600px;
    }
</style>