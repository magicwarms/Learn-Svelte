<script>
    async function getPosts() {
        const getPosts = await fetch(
            "https://jsonplaceholder.typicode.com/posts"
        );
        if (getPosts) return getPosts.json();
        else throw new Error("Failed to fetching the data");
    }
    let promise = getPosts();
    function handleClick() {
        promise = getPosts();
    }
</script>

<button on:click={handleClick}>Generate Data</button>

{#await promise}
    <p>Please wait....</p>
{:then getPosts}
    {#each getPosts as { id, title }}
        <p>{id}. {title}</p>
    {/each}
{:catch error}
    <p style="color: red">{error.message}</p>
{/await}
