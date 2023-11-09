<script>
    import {Link} from "svelte-routing";
  import Displayres from "./Displayres.svelte";
    import { mchart } from "./stores.js";
    
    let formval={
        cchart:'',

    }
    function checksubmit(){
alert("cchart"+formval);
mchart.update(value=>{
    return value=formval.cchart;
})
    }

    
</script>

<div class="row">
    <div class="col-md-1">
        <ul class="nav flex-column sidevav ">
           <!-- <ul class="navbar-nav mr-auto">-->
        <li class="nav-item dropdown customsidebar"><a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false"><span class="glyphicon glyphicon-th-large"></span><br>Widget</a>
            <div class="dropdown-menu" aria-labelledby="navbarDropdown">
           <a class="dropdown-item" href="#">widget 1</a>
            <a class="dropdown-item" href="#">widget2</a>

            </div>
        </li>
        <li class="nav-item dropdown customsidebar"><a class="nav-link dropdown-toggle" href="#" id="navbarDropdown2" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false"><span class="glyphicon glyphicon-signal"></span><br>Chart</a>
           <div class="dropdown-menu megamenu" aria-labelledby="navbarDropdown">
            <div class="modal-dialog modal-lg">
                <div class="modal-content">
                  
            <div class="row">
<button type="button" class="close" data-dismiss="modal" aria-label="Close">
            <span aria-hidden="true">&times;</span>
          </button>
        <form>
                <div class="col-md-3">
           <input type="radio" id="pie" value="pie" bind:group={formval.cchart}><a class="dropdown-item" href="#"><img width="150" height="150" src="data:image/jpeg;base64,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" alt="pie chart"/>
        </a>
        </div>
        <div class="col-md-3">
            <input type="radio" id="pie" value="bar" bind:group={formval.cchart}> <a class="dropdown-item" href="#"><img width="150" height="150" src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcROGoSb9tdB3FW2ra63vKd8rdaWMn9suyw7LA&usqp=CAU" alt="bar chart"/>
            </a>
            </div>
            <div class="col-md-3">
            <a class="dropdown-item" href="#"><img width="150" height="150" src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTQpflPnvzTKd6S7FpQkdk40edPuZ446Nsq5Q&usqp=CAU" alt="donut chart"/>
            </a>
            </div>
            
        
            <div class="col-md-3">

            <a class="dropdown-item" href="#"><img width="150" height="150" src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcROGoSb9tdB3FW2ra63vKd8rdaWMn9suyw7LA&usqp=CAU" alt="bar chart"/>
           </a>
            </div>
            <div class="col-md-3">

            <a class="dropdown-item" href="#"><img width="150" height="150" src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTQpflPnvzTKd6S7FpQkdk40edPuZ446Nsq5Q&usqp=CAU" alt="donut chart"/>
            </a>
            </div>
            
<button type="submit" class="btn btn-secondary"  data-dismiss="modal">Cancel</button>
          <button type="button" class="btn btn-primary" on:click={checksubmit} >Create</button>
        </form>
       </div>
       </div>
       </div>
            </div>
           <!--<Link to="/result">-->
        </li>
        <li class="nav-item dropdown customsidebar"><a class="nav-link dropdown-toggle" href="#" id="navbarDropdown3" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false"><span class="glyphicon glyphicon-signal"></span><br>Table</a>
            <div class="dropdown-menu" aria-labelledby="navbarDropdown">
           <a class="dropdown-item customdrop" href="#">Table1</a>
            <a class="dropdown-item" href="#">bar chart</a>

            </div>
        </li>
        <li class="nav-item customsidebar">
            <a class="nav-link" href="#"><span class="glyphicon glyphicon-signal"></span><br/>Text</a>
          </li>
          <li class="nav-item customsidebar">
            <a class="nav-link " href="#"><span class="glyphicon glyphicon-signal"></span><br/>Embed</a>
          </li>
          <li class="nav-item customsidebar">
            <a class="nav-link pb-8" href="#"><span class="glyphicon glyphicon-signal"></span><br/>Filter</a>
          </li>
         
                 <div class="navbottom"></div>
      </ul>
    </div>
    <div class="col-md-10">
<Displayres/>
</div>
</div>
<style>

.megamenu {
height: 400px;
width:800px
}
    img{
        border:1px solid gainsboro;
    }
    .customsidebar{
        padding-top: 15px;
        padding-bottom: 15px;
        color:whitesmoke;
        border-bottom: 2px solid whitesmoke;
    }
    .navbottom{
        padding-top:100%;
        padding-bottom: 100%;
    }
    .sidevav{
        background: #333;
    }
    .navbtn{
        background-color: #333;
        border:none;
        color:white;
    }
    .sidevav a:hover{
        background:#848484;
    }
    .sidevav a{
        color:white;
    }
.customsidebar:hover{
    background: #848484;
}

    span{
        margin-left: 34%;
    }
    .dropdown-menu{
        background: white;
    }
    .dropdown-menu .dropdown-item {
        color:black !important;
    }
</style>