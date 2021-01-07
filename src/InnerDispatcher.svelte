<script>
    import { createEventDispatcher } from "svelte";
    const eventDispatcher = createEventDispatcher();
    function sayHello() {
        eventDispatcher("dispatchHello", {
            text: "Hallo Ndan!",
        });
    }
</script>

<button on:click={sayHello}>Click dulu lah</button>
