<script>
    let csv;
    const handleClick = () => {
      const reader = new FileReader();
      reader.onload = () => {
        let txt = reader.result;
        console.log(txt);
      };
      reader.readAsText(csv);
  
      let json = csvJSON(csv);
  
    };
  
    function csvJSON(csv) {
      var lines = csv.split("\n");
      var result = [];
      var headers = lines[0].split(",");
      for (var i = 1; i < lines.length; i++) {
        var obj = {};
        var currentline = lines[i].split(",");
        for (var j = 0; j < headers.length; j++) {
          obj[headers[j]] = currentline[j];
        }
        result.push(obj);
      }
      console.log("result::");
      return JSON.stringify(result);
    }
  </script>
  
  <div class="container-sm mx-auto m-5 w-25">
    <div class="input-group">
      <input
        type="file"
        bind:value={csv}
        class="form-control"
        accept=".csv"
        id="inputGroupFile04"
        aria-describedby="inputGroupFileAddon04"
        aria-label="Upload"
      />
      <button
        class="btn btn-outline-secondary"
        on:click={handleClick}
        type="button"
        id="inputGroupFileAddon04">Go</button
      >
    </div>
  </div>
  