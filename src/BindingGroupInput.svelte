<script>
    let scoops = 1;
    let flavours = ["flavours"];

    let menu = [
        "Cookies and cream",
        "Mint choc chip",
        "Raspberry ripple",
        "Telek Kambing",
    ];

    function join(flavours) {
        if (flavours.length === 1) return flavours[0];
        return `${flavours.slice(0, -1).join(", ")} and ${
            flavours[flavours.length - 1]
        }`;
    }
    let totalScoops = 0;
    $: {
        if (scoops === 1) {
            totalScoops = 20;
        } else if (scoops === 2) {
            totalScoops = 40;
        } else if (scoops === 3) {
            totalScoops = 50;
        } else {
            totalScoops = 25;
        }
    }
</script>

<h2>Size</h2>

<label>
    <input type="radio" bind:group={scoops} value={1} />
    One scoop - $20
</label>

<label>
    <input type="radio" bind:group={scoops} value={2} />
    Two scoops - $40
</label>

<label>
    <input type="radio" bind:group={scoops} value={3} />
    Three scoops - $50
</label>

<label>
    <input type="radio" bind:group={scoops} value={4} />
    Half scoops - $25
</label>

<h2>Flavours</h2>

<!-- {#each menu as flavour} -->
<!-- <label>
        <input type="checkbox" bind:group={flavours} value={flavour} />
        {flavour}
    </label> -->
<!-- {/each} -->
<!-- for multiple choice using select multiple -->
<select multiple bind:value={flavours}>
    {#each menu as flavour}
        <option value={flavour}>{flavour}</option>
    {/each}
</select>

{#if flavours.length === 0}
    <p>Please select at least one flavour</p>
{:else if flavours.length > scoops}
    <p>Can't order more flavours than scoops!</p>
{:else}
    <p>
        You ordered
        {scoops}
        {scoops === 1 ? 'scoop' : 'scoops'}
        of
        {join(flavours)}
        <br />
        Total nya: ${totalScoops}
    </p>
{/if}
