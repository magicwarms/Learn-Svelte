<script>
  import { count } from "./Stores";
  const resetNumber = () => {
    count.set(0);
  };
</script>

<button on:click={resetNumber}>RESET</button>
