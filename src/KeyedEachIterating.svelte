<script>
    import Thing from "./Thing.svelte";

    let things = [
        { id: 1, color: "darkblue" },
        { id: 2, color: "indigo" },
        { id: 3, color: "deeppink" },
        { id: 4, color: "salmon" },
        { id: 5, color: "gold" },
    ];

    function handleClick() {
        things = things.slice(1);
    }
    $: remark = things.length > 0 ? "Remove baris pertama" : "HABIS WAK";
</script>

<button on:click={handleClick}>{remark}</button>

{#each things as thing (thing.id)}
    <Thing current={thing.color} number={thing.id} />
{/each}
