<script>
import Outer from "./Outer.svelte";
import Button from "./Button.svelte";
import MyapiCompo from "./MyapiCompo.svelte";
function handlegreet(event){
  alert(event.detail)
}

import Card from "./Card.svelte";
import NameList from "./NameList.svelte";
import Childcompo from "./Childcompo.svelte";
import MyautoFocus from "./MyautoFocus.svelte";
</script>

<main>
  <MyautoFocus/>

  <hr>
  <MyapiCompo />
<h3>app compo</h3>
  <Childcompo/>
<NameList>
  <h1 slot="hero" let:firstname let:lastname>{firstname} {lastname}</h1>
</NameList>

<hr>

<NameList>
  <h1 slot="hero" let:firstname let:lastname> {lastname} {firstname}</h1>
</NameList>

<hr>
<NameList>
  <h1 slot="hero" let:firstname let:lastname>{lastname}</h1>
</NameList>
  <Card>
    <div slot="header">
      <h1>header</h1>
    </div>
    <div slot="footer">
      <h1>footer</h1>
    </div><div slot="content">
      <h1>content</h1>
    </div>
  </Card>
  <h1>h</h1>
  <Outer on:greet={handlegreet}/>
  <Button on:click={()=>alert("clicked")}/>
</main>