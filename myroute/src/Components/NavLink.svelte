<script>
    import {Link} from 'svelte-routing';
</script>



  <div>
<nav class="navbar navbar-expand-lg navbar-light" style="background-color: #4399db;">

   <!--<nav class="navbar navbar-expand-lg mainnav">-->
        <!--<a class="navbar-brand" href="#">Navbar</a> -->
  <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNavDropdown" aria-controls="navbarNavDropdown" aria-expanded="false" aria-label="Toggle navigation">
    <span class="navbar-toggler-icon"></span>
  </button>
  <div class="collapse navbar-collapse" id="navbarNavDropdown">
    <ul class="navbar-nav">
        <li class="nav-item"> <Link to="/"><a class="nav-link" href="#">Home</a></Link> </li>
        <li class="nav-item"><Link to="/vishuallization"><a class="nav-link" href="#">vishuallization</a></Link></li>
        <li class="nav-item"><Link to="/contact"><a class="nav-link" href="#">Contact</a></Link></li>     
        <li class="nav-item"><Link to="/report"><a class="nav-link" href="#">Reports</a></Link></li>
        <li class="nav-item"><Link to="/data"><a class="nav-link" href="#">Data</a></Link></li>

        <li class="nav-item"><Link to="*"><a class="nav-link" href="#">Feedback</a></Link></li>
        <li class="nav-item dropdown homemainnavdrop"><a class="nav-link dropdown-toggle" href="#" id="navbarDropdown" role="button" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">dropdown1</a>
            <div class="dropdown-menu" aria-labelledby="navbarDropdown">
            <Link to="/action"><a class="dropdown-item" href="#">Action</a></Link>
            <Link to="/mypie"><a class="dropdown-item" href="#">Pie Charts</a></Link>
            <Link to="/mybar"><a class="dropdown-item" href="#">Bar Chart</a></Link>


            </div>
        </li>
      </ul>
    </div>
</nav>
</div>

<style>
  .mainnav{
    background: #4399db;
    color:white;
  }
  .mainnav a{
    color:white;
  }
  .homemainnavdrop {
    padding-top: 0;
  }

  navbar-nav li a{
    padding-top: 0;
  }
</style>
