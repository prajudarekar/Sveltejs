<script>

    // for ESM environment, need to import modules as:
     import bb, {pie} from "billboard.js";
      import { onMount } from "svelte";
    //let result=[];
    var data;
    onMount(async()=>{
      
     /* const res=await fetch("http://localhost:304/hyphenreport/user_account");
const result1=await res.json();*/


const response= await fetch("http://localhost:304/hyphenreport/user_account");
console.log("response:: "+response)
       data= await response.json();
       console.log(data);
       length=data.length;
       console.log(data);
       var temp="";
     /*  for(let i=0;i<length;i++)
       {
        
          console.log("role_id::"+data[i].role_id);
          console.log("Username::"+data[i].Username);
       }*/
/*const response= await fetch("https://www.thecocktaildb.com/api/json/v1/1/search.php?s=margarita%");
console.log("response:: "+response)
       const data= await response.json();
       console.log(data);
       length=data.drinks.length;
       console.log(data);
       var temp="";
       for(let i=0;i<length;i++)
       {
        
          console.log(data.drinks[i].strDrink);
          console.log(data.drinks[i].strInstructions);
       }
*/
/*for(let i=0;i<length;i++)
       {
        
          console.log("role_id::"+data[i].role_id);
          console.log("Username::"+data[i].Username);
       }*/
 for(var i=0;i<length;i++)    
{
  console.log("role_id::"+data[i].role_id);
var data2=[data[i].role_id,data[i].Username];
console.log("data2:: "+data2);
    var chart = bb.generate({
      
      data: {
        "columns": [
      [
        "data1",
        30
      ],
      [
        "data2",
        120
      ]
    ],
        type: pie(), // for ESM specify as: pie()
          },

          size:{
    height:420,
    width:420
  },
      bindto: "#pieChart"
    });
}


setTimeout(function () {
for(var i=0;i<length;i++)    
{
chart.load({

		columns: [
      [data[i].role_id,data[i].Username]
]
    });
}

}, 1500);

setTimeout(function () {
	chart.unload({
		ids: 'data1'
	});
	chart.unload({
		ids: 'data2'
	});
}, 2500);

    });
    
  
          </script>
          <div  id="pieChart"></div>
        