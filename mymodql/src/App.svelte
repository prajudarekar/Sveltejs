<script>
    import {Route,Router} from "svelte-routing";
    import Mynav from "./Mynav.svelte";
    import Home from "./Home.svelte";
    import Myreport from "./Myreport.svelte";
  
</script> 

<div>
    
    <Router>
        <Mynav/>
        <Route path="/" component={Home}/>
      <Route path="/report" component={Myreport}></Route>
      </Router>
    
</div>