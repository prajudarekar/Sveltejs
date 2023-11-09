<script>
    // for ESM environment, need to import modules as:
import bb, {donut} from "billboard.js";


var chart = bb.generate({
  data: {
    columns: [
	["data1", 30],
	["data2", 120]
    ],
    
    type: donut(), // for ESM specify as: donut()
    
    
  },
  donut: {
    title: "Iris Petal Width"
  },
  bindto: "#donutChart"
});

</script>
<div id="donutChart"></div>
