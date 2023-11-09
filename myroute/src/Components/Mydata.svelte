<script>
    import {onMount} from 'svelte';
    let result=[];
    onMount(async()=>{
        const res=await fetch("https://jsonplaceholder.typicode.com/todos");
        result=await res.json();
    })

</script>
<div>

    <h1>Employee Data Record Sheet</h1>

<div class="table-wrapper-scroll-y my-custom-scrollbar">
    
   <!--<table class="table table-bordered">-->
    <table class="table table-bordered table-striped mb-0" id="myTable">

        <thead class="thead-light">
        <tr class="header">
            <th scope="col">UserId</th>
            <th scope="col">Id</th>
            <th scope="col">Title</th>
            <th scope="col">Completed</th>

        </tr>
        </thead>
        {#each result as rs}
        <tr>
            <td>{rs.userId}</td>
            <td>{rs.id}</td>
            <td>{rs.title}</td>
            <td>{rs.completed}</td>

        </tr>
        {/each}
    </table>
</div>
</div>
<style>
    #myInput {
  background-image: url('/css/searchicon.png');
  background-position: 10px 10px;
  background-repeat: no-repeat;
  width: 100%;
  font-size: 16px;
  padding: 12px 20px 12px 40px;
  border: 1px solid #ddd;
  margin-bottom: 12px;
}
    h1{
        text-align: center;
    }
    table{
        margin-right:5%;
    }

    .my-custom-scrollbar {
position: relative;
height: 600px;
overflow: auto;
}
.table-wrapper-scroll-y {
display: block;
}

</style>