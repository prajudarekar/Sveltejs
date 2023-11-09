<script>
  import Menu from "./Components/Menu.svelte";
  import NewMenu from "./Components/NewMenu.svelte";
  import { Router, Route, Link } from "svelte-routing";
  import Home from './Components/Home.svelte';
import About from './Components/About.svelte';
  import { element } from "svelte/internal";
  import Notfound from "./Components/Notfound.svelte";
</script>

<div>
<Router>
  <Link to="/">Home</Link>
  <Link to="/about"> About</Link>
  <Link to="*"> Feedback</Link>


  <Route path="/" component={Home}></Route>
  <Route path="/about" component={About}></Route>
  <Route path="*" component={Notfound}></Route>


</Router>
</div>