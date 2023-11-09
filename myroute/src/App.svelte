<script>
  import {Router,Link,Route} from 'svelte-routing';
  import Home from './Components/Home.svelte';
  import About from './Components/About.svelte';
  import Contact from './Components/Contact.svelte';
  import Notfound from './Components/Notfound.svelte';
  import NavLink from './Components/NavLink.svelte';
  import Mychart from './Components/Mychart.svelte';
import Mydata from './Components/Mydata.svelte';
import Action from './ChartComponents/Action.svelte';
  import Mypie from './ChartComponents/Mypie.svelte';
  import Testchart from './ChartComponents/Testchart.svelte';
  import Myvishual from './Myvishual.svelte';
  import MyCreatevishual from './ChartContent/MyCreatevishual.svelte';
  import MybarChart from './ChartComponents/MybarChart.svelte';
  import MyMegaMenu from './ChartComponents/MyMegaMenu.svelte';
</script>

<div>
  <Router>
<NavLink/>
    <Route path="/" exact="true" component={Home}></Route>
    <Route path="/vishuallization" component={Myvishual}></Route>
    <Route path="/contact" component={Contact}></Route>
    <Route path="/report" component={Mychart}></Route>
    <Route path="/data" component={Mydata}></Route>

    <Route path="*" component={Notfound}></Route>
    <Route path="/action" component={Action}></Route>
    <Route path="/mypie" component={Mypie}></Route>
    <Route path="/Createvishual" component={MyCreatevishual}></Route>
    <Route path="/mybar" component={MybarChart}></Route>



    


  </Router>
</div>