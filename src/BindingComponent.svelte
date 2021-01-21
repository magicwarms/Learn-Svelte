<script>
  import { createEventDispatcher } from "svelte";

  export let value = "";

  const dispatch = createEventDispatcher();
  let select;
  $: select = (num) => {
    value += num;
    const valueSplit = value.split("");
    if (valueSplit.length > 4) {
      alert("Pin tidak boleh lebih dari 4 digit");
      value = valueSplit.splice(0, 4).join("");
    }
  };
  let clear;
  $: clear = () => (value = "");
  const submit = () => dispatch("submit");
</script>

<div class="keypad">
  <button on:click={select(1)}>1</button>
  <button on:click={select(2)}>2</button>
  <button on:click={select(3)}>3</button>
  <button on:click={select(4)}>4</button>
  <button on:click={select(5)}>5</button>
  <button on:click={select(6)}>6</button>
  <button on:click={select(7)}>7</button>
  <button on:click={select(8)}>8</button>
  <button on:click={select(9)}>9</button>

  <button disabled={!value} on:click={clear}>clear</button>
  <button on:click={select(0)}>0</button>
  <button disabled={!value} on:click={submit}>submit</button>
</div>

<style>
  .keypad {
    display: inline-grid;
    grid-template-columns: repeat(3, 5em);
    grid-template-rows: repeat(4, 3em);
    grid-gap: 0.5em;
  }

  button {
    margin: 0;
  }
</style>
