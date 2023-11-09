<script>
  import MyNavLink from "src/NavigationComponents/MyNavLink.svelte";
    import {Route,Router} from "svelte-routing";
  import Contact from "./Contact.svelte";
  import Home from "./Home.svelte";
  import Myvishual from "./Myvishual.svelte";
  import NotFoundPage from "./NotFoundPage.svelte";
</script>

<div>
<Router>
    <MyNavLink/>
        <Route path="/" exact="true" component={Home}></Route>
        <Route path="/vishuallization" component={Myvishual}></Route>
        <Route path="/contact" component={Contact}></Route>  
        <Route path="*" component={NotFoundPage}></Route>     

      </Router>
    </div>
    