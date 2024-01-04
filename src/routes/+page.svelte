<link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Amatic SC">

<script>
    import Cat from '../lib/Cat.svelte';
    import AboutPage from '../routes/about/+page.svelte'
    import WorkPage from '../routes/work/+page.svelte'
</script>


<style lang="scss">
    $color-black: #100c08;
    $color-white: #f4f3d7;
    $color-beige: #ecc298;

    $blink-purple: 0 0 5px #bf00ff, 0 0 15px #bf00ff, 0 0 20px #bf00ff, 0 0 40px #bf00ff, 0 0 60px #6f00ff, 0 0 10px #bf00ff, 0 0 98px #6f00ff;
    $blink-orange: 0 0 5px #FF9900, 0 0 15px #FF9900, 0 0 20px #FF9900, 0 0 40px #FF9900, 0 0 60px #ff0000, 0 0 10px #ff8d00, 0 0 98px #ff0000;
    $blink-brown: 0 0 5px rgb(95, 31, 31), 0 0 15px rgb(95, 31, 31), 0 0 20px rgb(95, 31, 31), 0 0 40px rgb(95, 31, 31), 0 0 60px brown, 0 0 10px rgb(95, 31, 31), 0 0 98px brown;

    :global(body) {
        background-color: $color-black;
        margin: 0;
    }

    #home-page {
        font-family: "Amatic SC", sans-serif;
        text-align: center;
        min-height: min(950px, 85vh);
        position: sticky;
        overflow: hidden;
    }

    .cat {
        padding-top: min(140px, 10vh);
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .name-intro {
        font-size: clamp(50px, 16vw, 120px);
        margin: 0;
        color: $color-beige;
    }

    .name {
        font-size: clamp(50px, 16vw, 120px);
        margin: 0;
        color: $color-white;
    }

    .subtitle {
        font-size:  clamp(25px, 4vw, 40px);
        margin-top: 40px;
        color: $color-white;
    }

    .aws-subtitle {
        line-height: clamp(25px, 6vw, 50px);
        text-shadow: $blink-orange;
        color: $color-white;
        text-align: center;
        animation: blinkorange 12s infinite;
    }

    .swe-subtitle {
        line-height: clamp(25px, 6vw, 40px);
        text-shadow: $blink-purple;
        color: $color-white;
        text-align: center;
        animation: blinkpurple 12s infinite;
    }
    
    .coffee-subtitle {
        line-height: clamp(25px, 6vw, 40px);
        text-shadow: $blink-brown;
        color: $color-white;
        text-align: center;
        animation: blinkbrown 12s infinite;
    }

    @keyframes blinkpurple {
        30%, 70%, 90% {
            color: $color-black;
            text-shadow: none;
        }
        0%,  29%, 31%, 69%, 71%, 89%, 91%, 100% {
            text-shadow: $blink-purple;
            color: white;
        }
    }

    @keyframes blinkorange {
        10%, 50%, 95% {
            color: $color-black;
            text-shadow: none;
        }
        0%, 9%, 11%, 49%, 51%, 95%, 96%, 100% {
            text-shadow: $blink-orange;
            color: white;
        }
    }

    @keyframes blinkbrown {
        30%, 60%, 80% {
            color: $color-black;
            text-shadow: none;
        }
        0%,  29%, 31%, 59%, 61%, 79%, 81%, 100% {
            text-shadow: $blink-brown;
            color: white;
        }
    }
</style>

<main>
    <div id="home-page">
        <div class="cat">
            <Cat/>
        </div>
        
        <p class="name"><span class="name-intro">Hi, I'm </span>Gajin</p>
        <!-- move this to below in the about me section -->
        <!-- <p class="subtitle">Software Consultant at Source Allies with <span class="aws-subtitle">4+ years of experience</span>. <br/>
            Specializing in <span class="aws-subtitle">AWS Cloud Architecture</span>, let's turn <b>bold ideas</b> into <b>reality</b>!
        </p> -->
        <p class="subtitle"> 
            /*
            <br>
            <b class="swe-subtitle">Software</b> 
            Engineer,
            <br>
            <b class="aws-subtitle">AWS Cloud</b>
            Enthusiast,
            <br>
            <b class="coffee-subtitle">Coffee & Boba </b>
            Extraordinaire
            <br>
            */
        </p>
    </div>
    <div id="about">
        <AboutPage /> <!-- add a section where i add my aws certificates-->
    </div>
    <div id="work">
        <WorkPage /> <!-- add a section where i add my aws certificates-->
    </div>
</main>