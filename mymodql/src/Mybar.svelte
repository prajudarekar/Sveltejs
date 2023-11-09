<script>
    // for ESM environment, need to import modules as:
 import bb, {bar} from "billboard.js";

 var chart = bb.generate({
    
    data: {
    x: "x",
    columns: [
        ["x", "www.siteone.com", "www.sitetwo.com", "www.sitethree.com", "www.sitefour.com"],
        ["downloads", 50, 100, 200, 600],
        ["uploads", 80, 110, 150, 220]
    ],
    groups: [
      [
        "downloads",
        "loading"
      ]
    ],
        colors: {
          downloads: "blue",
          uploads: "green"
        },
    type: bar(),
    },
    axis: {
        x: {
        type: "category"
        }
    },
    bindto: "#barChart_1"
    });

</script>

<div id="barChart_1"></div>