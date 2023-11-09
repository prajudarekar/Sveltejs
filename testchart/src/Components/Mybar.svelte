<script>
    // for ESM environment, need to import modules as:
 import bb, {bar} from "billboard.js";

 var chart = bb.generate({
    
    data: {
    x: "y",
    columns: [
        ["y", "www.siteone.com", "www.sitetwo.com", "www.sitethree.com", "www.sitefour.com"],
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
    
    padding: {
        top: 20,
        right: 10,
        bottom: 10,
        left: 50
      },
    axis: {
        x: {
        type: "category"
        }
    },
    size:{
    height:420,
    width:420

  },
    bindto: "#barChart_1"
    });
   
    

  /*  chart.resize({
   width: 640,
   height: 480
});*/

</script>
<div class="container">
  <div class="row">
  <div class="col-md-4">
<div class="card">
<div  id="barChart_1"></div>
</div>
</div>
</div>
</div>

<style>
    .card{
        border:2px solid green;
    }
</style>