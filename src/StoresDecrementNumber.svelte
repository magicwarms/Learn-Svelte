<script>
  import { count } from "./Stores";
  const decrementNumber = () => {
    count.update((val) => {
      return val - 1;
    });
  };
</script>

<button on:click={decrementNumber}>-</button>
