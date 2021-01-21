<script>
  import { onMount } from "svelte";
  let fetchGifData = [];
  onMount(async () => {
    try {
      const getGifs = await fetch(
        `https://api.giphy.com/v1/gifs/trending?api_key=&limit=25&rating=pg-13`
      );
      const gifData = await getGifs.json();
      fetchGifData = gifData.data;
    } catch (error) {
      console.error(error);
    }
  });
</script>

<div class="photos">
  {#each fetchGifData as gif}
    <figure>
      <img src={gif.images.original.webp} alt={gif.title} />
      <figcaption>{gif.title}</figcaption>
    </figure>
  {:else}
    <p>Please wait....</p>
  {/each}
</div>

<style>
  .photos {
    width: 100%;
    display: grid;
    grid-template-columns: repeat(5, 1fr);
    grid-gap: 8px;
  }

  figure,
  img {
    width: 100%;
    margin: 0;
  }
</style>
