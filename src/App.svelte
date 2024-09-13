<script>
// @ts-nocheck

  import Numbers from "./Numbers.svelte";
  import Nested from "./Nested.svelte";
  import Sibling1 from "./Sibling1.svelte";
  import Sibling2 from "./Sibling2.svelte";
  $: messageObject = {}

  function handleMessage(event){
    messageObject = event.detail
  }
</script>
 <Nested name='Srajan'/>
 <Numbers/>
 <Sibling1 on:siblingMessage={handleMessage} />
 <Sibling2 {messageObject}/>