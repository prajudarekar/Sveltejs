<script>
// for ESM environment, need to import modules as:
 import bb, {area, areaSpline, bar} from "billboard.js";


var chart = bb.generate({
  data: {
    columns: [
	["data1", 300, 350, 300, 0, 0, 0],
	["data2", 130, 100, 140, 200, 150, 50],

    ],
    types: {
      data1: area(), // for ESM specify as: area()
      data2: areaSpline(), // for ESM specify as: areaSpline()
      
    }
  },
  bindto: "#areaChart"
});
</script>



<div id="areaChart"></div>
