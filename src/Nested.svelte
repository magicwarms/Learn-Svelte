<script>
    import Info from "../src/Info.svelte";
    import Logic from "./Logic.svelte";
    // let imgUrl = "https://source.unsplash.com/random/400x200";
    let words = "Hello this word from nested component";
    // export let answer = "mencintai";
    export let theAnswer;
    const biodata = {
        name: "Yuna",
        birthdate: "09 July 2017",
        hobby: "Watch youtube",
    };
</script>

<style>
    .classP {
        font-family: Cambria, Cochin, Georgia, Times, "Times New Roman", serif;
    }
</style>

<p class="classP">{words}</p>
<!-- <img src={imgUrl} alt="Random pic from Unsplash API" /> -->
<p>Jawaban nya apa wak? {theAnswer}</p>
<Info {...biodata} />
<Logic />
