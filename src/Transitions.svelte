<script>
  import { fade, fly } from "svelte/transition";
  let visible = true;
</script>

<label for="checkbox">
  <input type="checkbox" bind:checked={visible} />
  Visible
</label>

{#if visible}
  <p transition:fade={{ duration: 1500 }}>
    Mamak aku cantik tapi ya gitu, gimana lagi ya kan hehe
  </p>
  <p transition:fly={{ y: 400, duration: 2000 }}>
    Bapak aku ganteng tapi ya gitu, gimana lagi ya kan hehe
  </p>
{/if}
<!-- ini untuk gabungin beberapa transisi di 1 line code -->
{#if visible}
  <p in:fly={{ y: 400, duration: 2000 }} out:fade={{ duration: 2000 }}>
    INI VERSI BARU LOOOOOH
  </p>
{/if}
