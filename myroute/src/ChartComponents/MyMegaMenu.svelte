



<div class="container">
    <div class="row">
     <div class="col-12">
      <nav class="navbar navbar-expand-lg navbar-light bg-light rounded">
       <a class="navbar-brand" href="#">Bootstrap 4 Mega Menu</a>
       <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbar" aria-controls="navbars" aria-expanded="false" aria-label="Toggle navigation">
                       <span class="navbar-toggler-icon"></span>
             </button>
       <div class="collapse navbar-collapse" id="navbar">
        <ul class="navbar-nav mr-auto">
         <li class="nav-item dropdown megamenu-li">
          <a class="nav-link dropdown-toggle" href="" id="dropdown01" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">Mega Menu 1</a>
          <div class="dropdown-menu megamenu" aria-labelledby="dropdown01">
           <div class="row">
            <div class="col-sm-6 col-lg-3">
             <h5>Links</h5>
             <a class="dropdown-item" href="#">Another action</a>
             <a class="dropdown-item" href="#">Something else here</a>
             <a class="dropdown-item" href="#">Another action</a>
             <a class="dropdown-item" href="#">Something else here</a>
            </div>
            <div class="col-sm-6 col-lg-3">
             <h5>More Links</h5>
             <a class="dropdown-item" href="#">Another action</a>
             <a class="dropdown-item" href="#">Something else here</a>
             <a class="dropdown-item" href="#">Another action</a>
            </div>
            <div class="col-sm-6 col-lg-3">
             <h5>Paragraph</h5>
             <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Necessitatibus in veritatis, facilis eligendi sunt, culpa autem harum porro earum.</p>
            </div>
            <div class="col-sm-6 col-lg-3">
             <h5>Image</h5>
             <img src="https://source.unsplash.com/250x150/?sig=4" alt="..." style="width: 100%;">
            </div>
           </div>
          </div>
         </li>
         <li class="nav-item dropdown megamenu-li">
          <a class="nav-link dropdown-toggle" href="" id="dropdown02" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">Mega Menu 2</a>
          <div class="dropdown-menu megamenu" aria-labelledby="dropdown02">
           <div class="row">
            <div class="col-sm-6 col-lg-4">
             <h5>Image Slider</h5>
             <div id="carouselExampleControls" class="carousel slide" data-ride="carousel">
              <div class="carousel-inner">
               <div class="carousel-item active">
                <img class="d-block w-100" src="https://source.unsplash.com/250x150/?sig=1" alt="...">
               </div>
               <div class="carousel-item">
                <img class="d-block w-100" src="https://source.unsplash.com/250x150/?sig=2" alt="...">
               </div>
               <div class="carousel-item">
                <img class="d-block w-100" src="https://source.unsplash.com/250x150/?sig=3" alt="...">
               </div>
              </div>
             </div>
            </div>
            <div class="col-sm-6 col-lg-3">
             <h5>Links</h5>
             <a class="dropdown-item" href="#">Another action</a>
             <a class="dropdown-item" href="#">Something else here</a>
             <a class="dropdown-item" href="#">Another action</a>
             <a class="dropdown-item" href="#">Something else here</a>
            </div>
            <div class="col-sm-6 col-lg-5">
             <h5>Paragraph</h5>
             <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Veniam impedit itaque minus distinctio possimus reiciendis et repellat. Voluptate, temporibus veniam et praesentium alias, maxime repudiandae aliquid, natus omnis animi iste!</p>
            </div>
           </div>
          </div>
         </li>
        </ul>
       </div>
      </nav>
     </div>
    </div>
   </div>

   <style>
    .megamenu-li {
	position: static;
}

.megamenu {
	position: absolute;
	width: 100%;
	left: 0;
	right: 0;
	padding: 15px;
}

   </style>