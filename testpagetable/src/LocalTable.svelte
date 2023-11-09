<script>
    //Row component is optional and only serves to render odd/even row, you can use <tr> instead.
    //Sort component is optional
    import { onMount } from "svelte";
    import Table, { Pagination, Row } from "./Table.svelte";
    
  
    let rows = [];
    let page = 0; //first page
    let pageSize = 10; //optional, 10 by default
  
    onMount(async () => {
     // rows = await fetch("");
      
      const res=await fetch("http://localhost:304/hyphenreport/user_account1");
      rows=await res.json();
    });
  
    function onCellClick(row) {
      alert(JSON.stringify(row));
    }
  
    
  </script>
  
  <Table {page} {pageSize} {rows} let:rows={rows2}>
    <thead slot="head">
      <tr>
        <th>
          Role_id
        </th>
        <th>
        Username
        </th>
       
      </tr>
    </thead>
    <tbody>
      {#each rows2 as row, index (row)}
        <Row {index} on:click={() => onCellClick(row)}>
          <td data-label="Name">{row.role_id}</td>
          <td data-label="Lastname">{row.Username}</td>
        </Row>
      {/each}
    </tbody>
  </Table>
  