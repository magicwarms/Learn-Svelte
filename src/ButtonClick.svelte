<script>
    let count = 0;
    let numbers = [1, 2, 3, 4];
    $: doubled = count * 2;
    $: console.log(`The count is ${count}`);
    $: if (count > 10) {
        alert(`It's dangerous, the count is ${count}`);
        count = 9;
    }
    const handleClick = () => (count += 1);
    $: if (numbers.length > 10) {
        alert(
            `It's dangerous, the length is already ${numbers.length}, back to 10`
        );
        numbers.pop();
    }
    const addNumber = () => (numbers = [...numbers, numbers.length + 1]);
</script>

<button on:click={handleClick}>Clicked
    {count}
    {count === 1 ? 'time' : 'times'}
</button>
<h1>{count} doubled is {doubled}</h1>

<button on:click={addNumber}>Add number click</button>

<h1>Added {numbers}</h1>
