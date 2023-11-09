<script>
import {bb, area,areaSpline, bar, zoom} from "billboard.js";
// base css
import "billboard.js/dist/theme/insight.css";

// for ESM environment, need to import modules as:
// import bb, {area, areaSpline} from "billboard.js";


var chart = bb.generate({
  data: {
    columns: [
	["data1", 300, 350, 300, 0, 0, 0],
	["data2", 130, 100, 140, 200, 150, 50]
    ],
    types: {
      data1: area(), 
	data2: areaSpline(), 
    }
  },
  bindto: "#areaChart"
});
</script>

<div id="areaChart"></div>
