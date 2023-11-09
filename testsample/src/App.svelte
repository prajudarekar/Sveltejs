<script>
  import {Router,Route} from "svelte-routing";
  import Home from "./Components/Home.svelte";
  import Myreport from "./Components/Myreport.svelte";
  import Mynav from "./Components/Mynav.svelte";
  import MyResult from "./ChartContent/MyResult.svelte";
  import Myform from "./Components/Myform.svelte";
</script>
<div>
<Router>
  <Mynav/>
  <Route path="/" component={Home}/>
  <Route path="/contact" component={Myreport}></Route>
<Route path="/result" component={MyResult}></Route>
</Router>
</div>