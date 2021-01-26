<script>
  import { count } from "./Stores";
  const incrementNumber = () => {
    count.update((val) => val + 1);
  };
</script>

<button on:click={incrementNumber}>+</button>
