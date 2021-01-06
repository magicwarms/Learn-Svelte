<script>
    let m = { x: 0, y: 0 };
    function handleMousemove(event) {
        m.x = event.clientX;
        m.y = event.clientY;
    }
    function handleClick() {
        alert("Apa kau");
    }
</script>

<style>
    div {
        width: 800px;
        height: 600px;
        background-color: black;
        color: wheat;
        margin: 0 auto;
        margin-bottom: 12px;
    }
</style>

<div on:mousemove={handleMousemove}>
    The mouse position is
    {m.x}
    x
    {m.y}
    <div><button on:click|once={handleClick}>Hello!</button></div>
</div>
