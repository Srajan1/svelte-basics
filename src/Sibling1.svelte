<script>
    import {createEventDispatcher} from 'svelte'
    const dispatch = createEventDispatcher()
    function dispatchMessage(){
        dispatch('siblingMessage', {
            'sender': 'sibling1',
            'text': 'Hey, what is up'
        })
    }
</script>

<button on:click={dispatchMessage}>dispatch message</button>