<script>
    import {count} from './script'
    function Increment(){
        count.update((n) => n+1)
    }

    function Decrement(){
        count.update((n) => n-1)
    }

    function Reset(){
        count.update((n) => n = 0)
    }
</script>

<button on:click={Increment}>Increment</button>
<button on:click={Decrement}>Decrement</button>
<button on:click={Reset}>Reset</button>

