<script>
    let imgUrl = "https://source.unsplash.com/random/400x200";
    let words = "Hello this word from nested component";
</script>

<style>
    .classP {
        font-family: Cambria, Cochin, Georgia, Times, "Times New Roman", serif;
    }
</style>

<p class="classP">{words}</p>
<img src={imgUrl} alt="Random pic from Unsplash API" />
