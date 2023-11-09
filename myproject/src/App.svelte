<script>
    import {Route,Router} from "svelte-routing";
  import Home from "./NorComponents/Home.svelte";
import Myvishual from "./NorComponents/Myvishual.svelte";
import Contact from "./NorComponents/Contact.svelte";
import NotFoundPage from "./NorComponents/NotFoundPage.svelte";
import MyNavLink from "./NavigationComponents/MyNavLink.svelte";
  import ReportVishualHome from "./NorComponents/ReportVishualHome.svelte";
</script>

<div>
<Router>
    <MyNavLink/>
        <Route path="/" exact="true" component={Home}></Route>
        <Route path="/vishuallization" component={Myvishual}></Route>
        <Route path="/contact" component={Contact}></Route>  
        <Route path="*" component={NotFoundPage}></Route>     
        <Route path="/Createvishual" component={ReportVishualHome}></Route>     


      </Router>
    </div>
    