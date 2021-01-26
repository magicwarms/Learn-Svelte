<script>
  import { tick } from "svelte";

  let text = `Select some text and hit the tab key to toggle uppercase`;

  async function handlingKeydown(event) {
    if (event.key !== "Shift") return;

    event.preventDefault();

    const { selectionStart, selectionEnd, value } = this;
    console.log("selectionStart", selectionStart);
    console.log("selectionEnd", selectionEnd);
    console.log("value", value);
    const selection = value.slice(selectionStart, selectionEnd);

    const replacement = /[a-z]/.test(selection)
      ? selection.toUpperCase()
      : selection.toLowerCase();

    text =
      value.slice(0, selectionStart) + replacement + value.slice(selectionEnd);

    await tick();
    this.selectionStart = selectionStart;
    this.selectionEnd = selectionEnd;
  }
</script>

<textarea value={text} on:keydown={handlingKeydown} />

<style>
  textarea {
    width: 100%;
    height: 200px;
  }
</style>
