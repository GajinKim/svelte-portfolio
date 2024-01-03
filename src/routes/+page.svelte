<script>
    import Cat from '../lib/Cat.svelte';
</script>

<link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Amatic SC">

<style>
    :global(body) {
        background-color: black;
    }

    main {
        font-family: "Amatic SC", sans-serif;
        text-align: center;
        padding-top: 20vh;
        padding-left: max(5px, 20vw);
        padding-right: max(5px, 20vw);
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
        margin: max(20px, 1.5vh);
        color: whitesmoke;
    }

    .aws-subtitle {
        font-size:  clamp(20px, 6vw, 40px);
        line-height: clamp(20px, 6vw, 40px);
        text-shadow: 0 0 5px #FF9900, 0 0 15px #FF9900, 0 0 20px #FF9900, 0 0 40px #FF9900, 0 0 60px #ff0000, 0 0 10px #ff8d00, 0 0 98px #ff0000;
        color: #fff6a9;
        text-align: center;
        animation: blinkorange 12s infinite;
    }

    @keyframes blinkorange {
        20%,24%,
        55% {
            color: black;
            text-shadow: none;
        }
        0%, 19%, 21%, 23%, 25%, 54%, 56%,
        100% {
        text-shadow: 0 0 5px #FF9900, 0 0 15px #FF9900, 0 0 20px #FF9900, 0 0 40px #FF9900, 0 0 60px #ff0000, 0 0 10px #ff8d00, 0 0 98px #ff0000;
            color: #fff6a9;
        }
    }
</style>

<main>
    <div class="cat">
        <Cat/>
    </div>
    <p class="name">Hello, I'm Gajin!</p>

    <!-- move this to below in the about me section -->
    <!-- <p class="subtitle">Software Consultant at Source Allies with <span class="aws-subtitle">4+ years of experience</span>. <br/>
        Specializing in <span class="aws-subtitle">AWS Cloud Architecture</span>, let's turn <b>bold ideas</b> into <b>reality</b>!
    </p> -->
    <p class="subtitle"><span class="software-subtitle">Software Consultant</span> , <span class="aws-subtitle">AWS</span> Enthusiast // Mentor</p>
</main>