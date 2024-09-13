<script>
    export let messageObject
</script>

{#if messageObject['text']}
    <p>{messageObject.text}</p>
{/if}