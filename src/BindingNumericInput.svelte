<script>
    let angka1 = 0;
    let angka2 = 0;
</script>

<input type="number" bind:value={angka1} min="0" max="12" />
<input type="range" bind:value={angka1} min="0" max="12" />

<input type="number" bind:value={angka2} min="0" max="12" />
<input type="range" bind:value={angka2} min="0" max="12" />

<h1>{angka1} + {angka2} = {angka1 + angka2}</h1>
