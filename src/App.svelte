<script>
// @ts-nocheck

  import Numbers from "./Numbers.svelte";
  import Nested from "./Nested.svelte";
  import Sibling1 from "./Sibling1.svelte";
  import Sibling2 from "./Sibling2.svelte";
  import Binding from "./Binding.svelte";

  import {count} from './script.js'
  import ModifyWritable from "./ModifyWritable.svelte";
  $: messageObject = {}

  function handleMessage(event){
    messageObject = event.detail
  }
  let count_value
  count.subscribe((value) => {
		count_value = value;
	});
</script>
 <Nested name='Srajan'/>
 <br>
 <br>
 <Numbers/>
 <br>
 <br>

 <Sibling1 on:siblingMessage={handleMessage} />
 <Sibling2 {messageObject}/>
 <br><br>

 <Binding/>
<br><br>
  <p>count is {count_value}</p>
 <ModifyWritable/>