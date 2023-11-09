<script>

    // for ESM environment, need to import modules as:
     import bb, {pie} from "billboard.js";
      import { onMount } from "svelte";
export let d1;
export let d2;
export let d3;


    onMount(()=>{
    var chart = bb.generate({
      data: {
        columns: [
        ["data1", d1],
        ["data2", d2],
        ["data3",d3]
        ],
        type: pie(), // for ESM specify as: pie()
        
      },
      bindto: "#pieChart"
    });
    });
    
          </script>
          
          <div id="pieChart"></div>
          
        