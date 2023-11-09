<script>
  import Mybar from "./Mybar.svelte";
  import Mypie from "./Mypie.svelte";
  import Mybar1 from "./Mybar1.svelte";
  import Mybar2 from "./Mybar2.svelte";
</script>


<div class="row">
  <div class="col-md-3 back">
    <Mypie/>
  </div>
  <div class="col-md-3 back">
    <Mybar/>
  </div>
  <div class="col-md-3 back1">
    <Mybar1/>
  </div>
  <div class="col-md-3 back1">
  <div class="card">
    <Mybar2/>
    </div>
  </div>
</div>

<style>
  .row{
    margin-left: 15px;
  }
  .back{
    background-color: white;
    width:200px;
    border:2px solid red;
  padding-left: 14px;

  }
  .back1{
    background-color: whitesmoke;
    width: 200px;
    border:2px solid gray;
  padding-left: 14px;

  }
</style>