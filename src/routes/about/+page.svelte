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
<h1>Skills</h1>

<SvelteLogo style="font-size:2em" />
<React style="font-size:2em" />
</main>
