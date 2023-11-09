<script>
    import {Link} from 'svelte-routing';
</script>

<div>
 <!--   <nav class="navbar navbar-expand-lg navbar-light bg-light">-->
        
<nav class="navbar navbar-expand-lg navbar-light" style="background-color: #4399db;">
        <a class="navbar-brand" href="#"> </a>
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
          <ul class="navbar-nav">
            <li class="nav-item active">
              <Link to="/"><a class="nav-link" href="#">Home <span class="sr-only">(current)</span></a></Link>
            </li>
          
            <li class="nav-item">
                <Link to="/vishuallization"><a class="nav-link" href="#">vishuallization</a></Link>
            </li>
            <li class="nav-item">
                <Link to="/contact"><a class="nav-link" href="#">Contact</a></Link>
            </li>

          
        </ul>
        </div>
      </nav>
</div>
        