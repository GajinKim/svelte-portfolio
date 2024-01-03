<script>
    import Cat from '../components/Cat.svelte';
</script>

<link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Alata">

<style>
    :global(body) {
        background-color: black;
    }

    body {
        font-family: "Alata", sans-serif;
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
        font-size: clamp(60px, 15vw, 110px);
        margin: 0;
        color: white;

    }

    .subtitle {
        font-size:  clamp(20px, 5vw, 40px);
        margin: 0;
        color: white;
    }


    .subtitle-item {
        animation: fadeIn 2s ease-in-out forwards;
    }
</style>

<body>
    <div class="cat">
        <Cat/>
    </div>
    <p class="name">GAJIN KIM</p>
    <p class="subtitle" ><span class="subtitle item" style="color:#FF9900;">AWS Cloud</span> Enthusiast</p>
</body>