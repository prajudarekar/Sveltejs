<script>
// for ESM environment, need to import modules as:
 import bb, {area, areaSpline} from "billboard.js";
 //import "billboard.js/dist/theme/insight.css";
 //import "billboard.js/dist/theme/default.css";
 import "billboard.js/dist/theme/datalab.css";
 //import "billboard.js/dist/theme/graph.css";


var chart = bb.generate({
  data: {
    columns: [
	["data1", 300, 350, 300, 0, 0, 0],
	["data2", 130, 100, 140, 200, 150, 50]
    ],
    types: {
      data1: area(), // for ESM specify as: area()
      data2: areaSpline(), // for ESM specify as: areaSpline()
    }
  },
  tooltip: {
    show: true
  },
  axis: {
  x: {
    show: true
  }
},
  bindto: "#areaChart"
});

  </script>
  
  
  
  <div class="cchart" id="areaChart"></div>

  