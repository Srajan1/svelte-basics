<script>
    $: numbers = [1]
</script>

{#each numbers as number}
    <span>{number + ' '}</span>
{/each}
<br>
<button on:click={() => {{numbers = [...numbers, numbers.push(numbers.length+1)]} }}>
    Add Number
</button>

