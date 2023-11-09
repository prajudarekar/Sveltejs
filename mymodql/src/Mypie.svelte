<script>

    // for ESM environment, need to import modules as:
     import bb, {pie} from "billboard.js";
      import { onMount } from "svelte";
    
    onMount(()=>{
    var chart = bb.generate({
      data: {
        columns: [
        ["data1", 30],
        ["data2", 120],
        ["data3",60]
        ],
        type: pie(), // for ESM specify as: pie()
        colors:{
            data1:"red",
            data2:"blue",
            data3:"purple"
    
        },
       /* onclick: function(d, i) {
        console.log("onclick", d, i);
       },
        onover: function(d, i) {
        console.log("onover", d, i);
       },
        onout: function(d, i) {
        console.log("onout", d, i);
       }*/
      },
      bindto: "#pieChart"
    });
    });
    
    
          </script>
          <div id="pieChart" ></div>
        
          <style>
            
          </style>