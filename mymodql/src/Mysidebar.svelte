<script>

    import { mchart, tablename } from "./stores.js";
    import Myform from "./Myform.svelte";
    import Displayresult from "./Displayresult.svelte";
    import DisplayTablecontant from "./DisplayTablecontant.svelte";
    import Mytableform from "./Mytableform.svelte";
    import MyTab from "./MyTab.svelte";
  import Modal from "./Modal.svelte";
  
     let formval={
         cchart:'',
     }
     let formval1={
         tablename:'',
     }
 function mysubmit(){
   mchart.update(value=>{
    alert("submit:: "+formval.cchart);
     return value=formval.cchart;
 })
 
 }
 //document.getElementById("btn1").addEventListener("click", mytable);

 function mytable(){
  
   tablename.update(value=>{
  alert("submit table:: "+formval1.tablename);
     return value=formval1.tablename;
 });
}

//document.addEventListener("click", mytable);

 
</script>

<div class="row">

    <div class="col-md-1">
        <ul class="nav flex-column sidevav ">
           <!-- <ul class="navbar-nav mr-auto">-->
        <li class="nav-item dropdown customsidebar">
            <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false"><span class="glyphicon glyphicon-th-large"></span><br>Widget</a>
            <div class="dropdown-menu" aria-labelledby="navbarDropdown">
           <a class="dropdown-item" href="#">widget 1</a>
            <a class="dropdown-item" href="#">widget2</a>

            </div>
        </li>
        <li class="nav-item customsidebar">
            <!-- Button trigger modal -->
  <button type="button" class="nav-link navbtn " data-toggle="modal" data-target="#exampleModal">
      Charts
    </button>
    </li>
    <!-- Modal -->
    
    <div class="modal fade" id="exampleModal" role="dialog" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
      <div class="modal-dialog modal-lg">
        <div class="modal-content">
          <div class="modal-header">
            <h5 class="modal-title" id="exampleModalLabel"> Charts</h5>
            <button type="button" class="close" data-dismiss="modal" aria-label="Close">
              <span aria-hidden="true">&times;</span>
            </button>
          </div>
         <!-- <div class="modal-body">-->
          <div class="modal-body">
            <form >
                <div class="row">
                <div class="col-md-3 card">
            <input type="radio" id="pie" name="chartname" value="pie" bind:group={formval.cchart} />
            <label for="pie" width="120" height="120">
            </label>
            </div>
        
            <div class="col-md-3 card">
           <input type="radio" id="bar" name="chartname" value="bar" bind:group={formval.cchart}/>
           <label for="bar" width="120" height="120">
            </label>
        </div>
        
        <div class="col-md-3 card">
            <input type="radio" id="donut" name="chartname" value="donut" bind:group={formval.cchart}/>
           <label for="donut" width="120" height="120">
           </label>
        </div>
        </div>
           
           <input type="button" id="submit" class="btn btn-primary" on:click={mysubmit} data-dismiss="modal"  value="Create" >

           <input type="button" class="btn btn-secondary" data-dismiss="modal" value="Cancel" >
        
        </form>  
        </div>
      </div>
    </div>    
</div>


        

<li class="nav-item customsidebar">
            <a class="nav-link" href="#"><span class="glyphicon glyphicon-signal"></span><br/>Text</a>
          </li>


          <li class="nav-item customsidebar">
            <!-- Button trigger modal -->
  <button type="button" class="nav-link navbtn " data-toggle="modal" data-target="#tableModal">
      Tables
    </button>
    </li>
    <!-- Modal -->
    
    <div class="modal fade" id="tableModal" role="dialog" tabindex="-1" aria-labelledby="tableModalLabel" aria-hidden="true">
      <div class="modal-dialog modal-lg">
        <div class="modal-content">
          <div class="modal-header">
            <h5 class="modal-title" id="tableModalLabel"> Table</h5>
            <button type="button" class="close" data-dismiss="modal" aria-label="Close">
              <span aria-hidden="true">&times;</span>
            </button>
          </div>
         <!-- <div class="modal-body">-->
          <div class="modal-body">
            
    <form >
        <div class="row">
        <div class="col-md-3 card">
    <input type="radio" id="tablenormal" name="tablename" value="tablenormal" bind:group={formval1.tablename} />
    <label for="tablenormal" width="120" height="120">
    </label>
    </div>

    <div class="col-md-3 card">
   <input type="radio" id="tabledarkheaderanborder" name="tablename" value="tabledarkheaderanborder" bind:group={formval1.tablename}/>
   <label for="tabledarkheaderanborder" width="120" height="120">
    </label>
</div>

<div class="col-md-3 card">
    <input type="radio" id="tabledarkhead" name="tablename" value="tabledarkhead" bind:group={formval1.tablename}/>
   <label for="tabledarkhead" width="120" height="120">
   </label>
</div>
</div>
   
<div class="col-md-3 card">
    <input type="radio" id="tabledark" name="tablename" value="tabledark" bind:group={formval1.tablename}/>
   <label for="tabledark" width="120" height="120">
   </label>
</div>

   <input type="button" id="btn1" class="btn  btn-primary " on:click={mytable} data-dismiss="modal" value="Submit"  >
   <input type="button" class="btn btn-secondary" data-dismiss="modal" value="Cancel" >
   </form>
        </div>
      </div>
    </div>    
</div>


          
          
          
          <li class="nav-item customsidebar">
            <a class="nav-link " href="#"><span class="glyphicon glyphicon-signal"></span><br/>Embed</a>
          </li>
          <li class="nav-item customsidebar">
            <a class="nav-link pb-8" href="#"><span class="glyphicon glyphicon-signal"></span><br/>Filter</a>
          </li>
              <li class="nav-item dropdown customsidebar">
            <a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false"><span class="glyphicon glyphicon-th-large"></span><br>Table</a>
            <div class="dropdown-menu" aria-labelledby="navbarDropdown">
         <Mytableform/>

            </div>
        </li>
         
                 <div class="navbottom"></div>
      </ul>
    </div>
    <div class="col-md-11">
      <MyTab/>
     <!-- <DisplayTablecontant/>
      <Displayresult/>-->
</div>
</div>
<style>
	
  :global(body.dark-mode) .customsidebar {
		background-color:#3c81b5;
		color: white;
	}
  
  :global(body.dark-mode) .sidevav a {
		background-color:#3c81b5;
		color: white;
	}
  
  :global(body.dark-mode) .navbtn  {
    background-color:#3c81b5;
		color: white;
	}
  
    .customsidebar{
      background: #333;
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


    input[type="radio"]{
display:none;
}
.card{
    margin-top:15px;
    width:250px;
    height:250px;
margin-left:2%;
border:none;
}
/*table card Module css*/

#tablenormal[type="radio"] + label
{
background-image: url("C:\Users\USER\Desktop\Sveltejs\mymodql\src\Tablenormal.png");
height: 150px;
width: 150px;
display:inline-block;
padding: 0 0 0 0px;
border:2px solid gainsboro;
}

#tablenormal[type="radio"]:checked + label
{
background-image:url("C:\Users\USER\Desktop\Sveltejs\mymodql\src\Tablenormal.png"); 
height: 150px;
width: 150px;
display:inline-block;
padding: 0 0 0 0px;
box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 #3c81b5;
}


#tabledarkheaderanborder[type="radio"] + label
{
background-image: url("C:\Users\USER\Desktop\Sveltejs\mymodql\src\Tabledarkheaderanborder.png");
height: 150px;
width: 150px;
display:inline-block;
padding: 0 0 0 0px;
border:2px solid gainsboro;
}

#tabledarkheaderanborder[type="radio"]:checked + label
{
background-image:url("C:\Users\USER\Desktop\Sveltejs\mymodql\src\Tabledarkheaderanborder.png"); 
height: 150px;
width: 150px;
display:inline-block;
padding: 0 0 0 0px;
box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 #3c81b5;

}
#tabledarkhead[type="radio"] + label
{
background-image:url("C:\Users\USER\Desktop\Sveltejs\mymodql\src\Tabledarkhead.png");
height: 150px;
width: 150px;
display:inline-block;
padding: 0 0 0 0px;
border:2px solid gainsboro;
}

#tabledarkhead[type="radio"]:checked + label
{
background-image:url("C:\Users\USER\Desktop\Sveltejs\mymodql\src\Tabledarkhead.png");
height: 150px;
width: 150px;
display:inline-block;
padding: 0 0 0 0px;
box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 #3c81b5;

}
#tabledark[type="radio"] + label
{
background-image:url("C:\Users\USER\Desktop\Sveltejs\mymodql\src\Tabledark.png");
height: 150px;
width: 150px;
display:inline-block;
padding: 0 0 0 0px;
border:2px solid gainsboro;
}

#tabledark[type="radio"]:checked + label
{
background-image:url("C:\Users\USER\Desktop\Sveltejs\mymodql\src\Tabledark.png");
height: 150px;
width: 150px;
display:inline-block;
padding: 0 0 0 0px;
box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 #3c81b5;

}


#pie[type="radio"] + label
{
background-image: url("C:\Users\USER\Desktop\Sveltejs\mymodql\src\bar.png");
height: 150px;
width: 150px;
display:inline-block;
padding: 0 0 0 0px;
border:2px solid gainsboro;
}

#pie[type="radio"]:checked + label
{
background-image:url("C:\Users\USER\Desktop\Sveltejs\mymodql\src\bar.png"); 
height: 150px;
width: 150px;
display:inline-block;
padding: 0 0 0 0px;
box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 #3c81b5;
}


#bar[type="radio"] + label
{
background-image: url("C:\Users\USER\Desktop\Sveltejs\mymodql\src\bar (2).png");
height: 150px;
width: 150px;
display:inline-block;
padding: 0 0 0 0px;
border:2px solid gainsboro;
}

#bar[type="radio"]:checked + label
{
background-image:url("C:\Users\USER\Desktop\Sveltejs\mymodql\src\bar (2).png"); 
height: 150px;
width: 150px;
display:inline-block;
padding: 0 0 0 0px;
box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 #3c81b5;

}
#donut[type="radio"] + label
{
background-image:url("C:\Users\USER\Desktop\Sveltejs\mymodql\src\donut.png");
height: 150px;
width: 150px;
display:inline-block;
padding: 0 0 0 0px;
border:2px solid gainsboro;
}

#donut[type="radio"]:checked + label
{
background-image:url("C:\Users\USER\Desktop\Sveltejs\mymodql\src\donut.png");
height: 150px;
width: 150px;
display:inline-block;
padding: 0 0 0 0px;
box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 #3c81b5;

}


/*table card Module css*/

#tablenormal[type="radio"] + label
{
background-image: url("C:\Users\USER\Desktop\Sveltejs\mymodql\src\Tablenormal.png");
height: 150px;
width: 150px;
display:inline-block;
padding: 0 0 0 0px;
border:2px solid gainsboro;
}

#tablenormal[type="radio"]:checked + label
{
background-image:url("C:\Users\USER\Desktop\Sveltejs\mymodql\src\Tablenormal.png"); 
height: 150px;
width: 150px;
display:inline-block;
padding: 0 0 0 0px;
box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 #3c81b5;
}


#tabledarkheaderanborder[type="radio"] + label
{
background-image: url("C:\Users\USER\Desktop\Sveltejs\mymodql\src\Tabledarkheaderanborder.png");
height: 150px;
width: 150px;
display:inline-block;
padding: 0 0 0 0px;
border:2px solid gainsboro;
}

#tabledarkheaderanborder[type="radio"]:checked + label
{
background-image:url("C:\Users\USER\Desktop\Sveltejs\mymodql\src\Tabledarkheaderanborder.png"); 
height: 150px;
width: 150px;
display:inline-block;
padding: 0 0 0 0px;
box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 #3c81b5;

}
#tabledarkhead[type="radio"] + label
{
background-image:url("C:\Users\USER\Desktop\Sveltejs\mymodql\src\Tabledarkhead.png");
height: 150px;
width: 150px;
display:inline-block;
padding: 0 0 0 0px;
border:2px solid gainsboro;
}

#tabledarkhead[type="radio"]:checked + label
{
background-image:url("C:\Users\USER\Desktop\Sveltejs\mymodql\src\Tabledarkhead.png");
height: 150px;
width: 150px;
display:inline-block;
padding: 0 0 0 0px;
box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 #3c81b5;

}
#tabledark[type="radio"] + label
{
background-image:url("C:\Users\USER\Desktop\Sveltejs\mymodql\src\Tabledark.png");
height: 150px;
width: 150px;
display:inline-block;
padding: 0 0 0 0px;
border:2px solid gainsboro;
}

#tabledark[type="radio"]:checked + label
{
background-image:url("C:\Users\USER\Desktop\Sveltejs\mymodql\src\Tabledark.png");
height: 150px;
width: 150px;
display:inline-block;
padding: 0 0 0 0px;
box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 #3c81b5;

}

</style>
