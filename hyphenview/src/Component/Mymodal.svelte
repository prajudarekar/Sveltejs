
<!-- Modal -->
    
<div class="modal fade" id="exampleModal" role="dialog" tabindex="-1" aria-labelledby="exampleModalLabel" aria-hidden="true">
    <div class="modal-dialog modal-lg">
      <div class="modal-content">
        <div class="modal-header">
          <h5 class="modal-title" id="exampleModalLabel"> Charts</h5>
          <button type="button" class="close" data-dismiss="modal" aria-label="Close">
            <span aria-hidden="true">&times;</span>
          </button>
        </div>
       <!-- <div class="modal-body">-->
        <div class="modal-body">
          <form >
              <div class="row">
              <div class="col-md-3 card">
          <input type="radio" id="pie" name="chartname" value="pie" bind:group={formval.cchart} />
          <label for="pie" width="120" height="120">
          </label>
          </div>
      
          <div class="col-md-3 card">
         <input type="radio" id="bar" name="chartname" value="bar" bind:group={formval.cchart}/>
         <label for="bar" width="120" height="120">
          </label>
      </div>
      
      <div class="col-md-3 card">
          <input type="radio" id="donut" name="chartname" value="donut" bind:group={formval.cchart}/>
         <label for="donut" width="120" height="120">
         </label>
      </div>
      </div>
         
         <input type="button" id="submit" class="btn btn-primary" on:click={mysubmit} data-dismiss="modal"  value="Create" >
  
         <input type="button" class="btn btn-secondary" data-dismiss="modal" value="Cancel" >
      
      </form>  
      </div>
    </div>
  </div>    
  </div>
  