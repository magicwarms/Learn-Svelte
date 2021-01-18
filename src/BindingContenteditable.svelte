<script>
    let html = "<p>Hallo wak napa tu</p>";
</script>

<style>
    [contenteditable] {
        padding: 0.5em;
        border: 1px solid #eee;
        border-radius: 4px;
    }
</style>

<div bind:innerHTML={html} contenteditable="true" />

<pre>{html}</pre>
