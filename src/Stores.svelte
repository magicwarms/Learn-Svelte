<script>
  import { count } from "./Stores";
  import StoresDecrementNumber from "./StoresDecrementNumber.svelte";
  import StoresIncrementNumber from "./StoresIncrementNumber.svelte";
  import StoresResetNumber from "./StoresResetNumber.svelte";
</script>

<h1>The counts is {$count < 0 ? count.set(0) : $count}</h1>

<StoresIncrementNumber />
<StoresDecrementNumber />
<StoresResetNumber />
