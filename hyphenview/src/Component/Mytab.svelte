<script>
  import DisplayTablecontent from "./DisplayTablecontent.svelte";
  import Displayresult from "./Displayresult.svelte";
</script>

<div class="container-fluid custum">
<!-- Nav tabs -->
<ul class="nav nav-tabs" id="myTab" role="tablist">
  <li class="nav-item">
    <a class="nav-link active" id="home-tab" data-toggle="tab" href="#home" role="tab" aria-controls="home" aria-selected="true">Home</a>
  </li>
  <li class="nav-item">
    <a class="nav-link" id="profile-tab" data-toggle="tab" href="#profile" role="tab" aria-controls="profile" aria-selected="false">Profile</a>
  </li>
  <li class="nav-item">
    <a class="nav-link" id="messages-tab" data-toggle="tab" href="#messages" role="tab" aria-controls="messages" aria-selected="false">Messages</a>
  </li>
  <li class="nav-item">
    <a class="nav-link" id="settings-tab" data-toggle="tab" href="#settings" role="tab" aria-controls="settings" aria-selected="false">Settings</a>
  </li>
</ul>

<!-- Tab panes -->
<div class="tab-content"   style="position:relative;">
  <div class="tab-pane active" id="home" role="tabpanel" aria-labelledby="home-tab">
   
    <Displayresult/>
  
    <DisplayTablecontent/>
  
  </div>
  <div class="tab-pane" id="profile" role="tabpanel" aria-labelledby="profile-tab">...</div>
  <div class="tab-pane" id="messages" role="tabpanel" aria-labelledby="messages-tab">...</div>
  <div class="tab-pane" id="settings" role="tabpanel" aria-labelledby="settings-tab">...</div>
</div>
</div>

<style>
  .custum{
    border:2px solid gainsboro;
    height: 100%;
  }
  /*
:global(svg .cardbar ){
    position: absolute;
    left:25%;
    bottom: 35%;
    background: white;
    border:2px solid gainsboro;
  }*/
</style>