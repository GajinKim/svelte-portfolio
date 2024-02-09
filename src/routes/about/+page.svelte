<script>
    import SvelteLogo from 'virtual:icons/logos/svelte-icon'; // logos:svelte-icon
    import React from 'virtual:icons/logos/react'; // logos:svelte-icon

    // import Icon from 'virtual:icons/foo/icon-name';
    
</script>

<style lang="scss">
    $color-black: #100c08;
    $color-white: #f4f3d7;
    $color-beige: #ecc298;

    main {
        font-family: "Amatic SC", sans-serif;
        text-align: left;
        padding-top: min(140px, 10vh);
        padding-bottom: min(140px, 10vh);
        padding-left: max(5px, 20vw);
        padding-right: max(5px, 20vw);

        background-color: $color-beige;
        position: sticky;
        overflow: hidden;
    }
</style>

<main>
<h1>About Me</h1>
<p>Back in 2012, I decided to try my hand at creating custom Tumblr themes and tumbled head first into the rabbit hole of coding and web development. Fast-forward to today, and I’ve had the privilege of building software for an advertising agency, a start-up, a student-led design studio, and a huge corporation.
    <br>
    <br>

    My main focus these days is building products and leading projects for our clients at Upstatement. In my free time I've also released an online video course that covers everything you need to know to build a web app with the Spotify API.
    <br>
    <br>
    When I’m not at the computer, I’m usually rock climbing, hanging out with my wife and two cats, or running around Hyrule searching for Korok seeds
    </p>
    <br>
<h1>Skills</h1>

<SvelteLogo style="font-size:2em" />
<React style="font-size:2em" />
</main>