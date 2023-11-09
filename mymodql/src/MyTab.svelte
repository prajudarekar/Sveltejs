<script>
    import {Tabs, Tab, TabList, TabPanel}  from 'svelte-tabs';
    
    import Displayresult from "./Displayresult.svelte";
    import DisplayTablecontant from "./DisplayTablecontant.svelte";
    import Mymode from "./Mymode.svelte";

  </script> 
   <div>
  <Tabs class="Tabs">
    <TabList>
      <Tab>One</Tab>
      <Tab>Two</Tab>
      <Tab>Three</Tab>
      <Tab>Three8</Tab>

    </TabList>
   
    <TabPanel>
        <DisplayTablecontant/>
        <Displayresult/>
    </TabPanel>
   
    <TabPanel>
      <h2>Panel Two</h2>
    </TabPanel>
   
    <TabPanel>
      <h2>Panel Three</h2>
    </TabPanel>
    
    <TabPanel>
      <h2>Panel other</h2>
    </TabPanel>
  </Tabs>
</div>
  <style>
   /* 
  :global(body.dark-mode) div {
		background-color:#333;
		color: white;
	}*/
  </style>