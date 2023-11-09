<script>
    // for ESM environment, need to import modules as:
 import bb, {bar} from "billboard.js";


var chart = bb.generate({
  data: {
    
    columns: [
	["data1", 30, 200, 100, 400, 150, 250],
	["data2", 130, 100, 140, 200, 150, 50]
    ],
    type: bar(), // for ESM specify as: bar()
  },
  size: {
    height: 600,
    width: 780
  },
  bar: {
    width: {
      ratio: 0.5
    }
  },
  bindto: "#barChart_1"
});

</script>

<div id="barChart_1"></div>