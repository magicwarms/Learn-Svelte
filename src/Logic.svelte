<script>
    import Iterate from "./Iterate.svelte";

    let user = { loggedIn: false };
    const toggle = () => {
        console.info(`user is logged in: ${!user.loggedIn}`);
        user.loggedIn = !user.loggedIn;
    };
    const x = 90;
</script>

<style>
    .fontRed {
        color: red;
    }
    .fontYellow {
        color: darkblue;
    }
    .fontBlack {
        color: black;
    }
</style>

{#if user.loggedIn}
    <button on:click={toggle}>Logout</button>
{:else}<button on:click={toggle}>Login</button>{/if}

{#if x > 90}
    <p class="fontRed">Nilai mu: {x} Magnificent</p>
{:else if x > 50 && x <= 90}
    <p class="fontYellow">Nilai mu: {x} Not Bad</p>
{:else}
    <p class="fontBlack">Nilai mu: {x} Bodoh kau</p>
{/if}

<Iterate />
