<script>
    $: numbers = [1]
</script>

{#each numbers as number}
    <p>{number}</p>
{/each}

<button on:click={() => {{numbers = [...numbers, numbers.push(numbers.length+1)]} }}>
    press me
</button>

