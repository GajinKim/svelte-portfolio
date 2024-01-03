<script>
    import Cat from '../lib/Cat.svelte';
</script>

<link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Signika">

<style>
    :global(body) {
        background-color: black;
    }

    main {
        font-family: "Signika", sans-serif;
        text-align: center;
        padding-top: 25vh;
        padding-left: min(5px, 5vw);
        padding-right: min(5px, 5vw);
    }

    .cat {
        display: flex;
        justify-content: center; /* Center horizontally */
        align-items: center; /* Center vertically */
    }

    .name {
        font-size: clamp(50px, 15vw, 100px);
        margin: 0;
        color: whitesmoke;

    }

    .subtitle {
        font-size:  clamp(20px, 6vw, 40px);
        margin: 0;
        color: whitesmoke;
    }
</style>

<main>
    <div class="cat">
        <Cat/>
    </div>
    <p class="name">Gajin Kim</p>
    <p class="subtitle" ><span class="subtitle item" style="color:#FF9900;">AWS Cloud</span> Enthusiast</p>
</main>