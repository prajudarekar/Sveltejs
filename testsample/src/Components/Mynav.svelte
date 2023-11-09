<script>
    import {Link} from "svelte-routing";

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
            <li class="nav-item"> <Link to=""><a class="nav-link" href="#">Home</a></Link></li>
            <li class="nav-item"><Link to="/contact"><a class="nav-link" href="#">Report</a></Link></li>
</ul>
</div>
</nav>
</div>