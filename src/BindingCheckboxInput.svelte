<script>
    let info = false;
    $: infoHadiah = info
        ? "Ayo sini nonton bokep"
        : "Check diatas dulu, ntar dapat hadiah loh";
    function alertPrank() {
        alert("Tobat lah kau anak muda");
    }
</script>

<style>
    .optionNo {
        color: red;
        font-family: Arial, Helvetica, sans-serif;
    }

    .optionYes {
        color: black;
        font-family: "Courier New", Courier, monospace;
    }
</style>

<input type="checkbox" bind:checked={info} />
Ayo CHECK SINI!
{#if info}
    <h1 class="optionYes">Bagus kau sudah mengikuti kata ku! HAHA</h1>
{:else}
    <h2 class="optionNo">
        Kau harus check info diatas, kalo gak aku bunuh kau!
    </h2>
{/if}

<button disabled={!info} on:click|once={alertPrank}>{infoHadiah}</button><br />
