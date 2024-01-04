<link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Amatic SC">

<script>
    import { base } from '$app/paths';
</script>

<nav class="navbar">
    <a class="navbar-item" href="{base}/">
        <span class="navbar-slashes">//</span> 
        <span class="navbar-text">HOME</span>
    </a>
    <a class="navbar-item" href="{base}/#about"><span class="navbar-slashes">//</span> <span class="navbar-text">ABOUT</span></a>
    <a class="navbar-item" href="{base}/#work"><span class="navbar-slashes">//</span> <span class="navbar-text">WORK</span></a>
    <a class="navbar-item" href="https://github.com/gajinkim"><span class="navbar-slashes">//</span> <span class="navbar-text">GITHUB</span></a>
</nav>

<style lang="scss">
    $color-black: #100c08;
    $color-white: #f4f3d7;
    $color-beige: #ecc298;

    .navbar {
        font-family: "Amatic SC", sans-serif;
        font-size:  clamp(25px, 4vw, 30px);
        font-weight: bold;

        display: flex;
        justify-content: space-evenly;
        position: sticky;

        padding-top: max(50px, 2vh);
        padding-bottom: max(50px, 2vh);
        @media (pointer:fine) {
            padding-left: 20vw;
            padding-right: 20vw;
        }
    }

    .navbar-item {
        text-decoration: none; 
        color: $color-beige;
        padding: 0 .25rem;
        transition: color 0.3s ease-in-out, box-shadow 0.3s ease-in-out;
    }
    @media (pointer:none), (pointer:coarse) {
        .navbar-slashes {
            display: none;
        }
    }

    @media (pointer:fine) {
        .navbar-slashes {
            color: $color-white;
            transition: color 0.3s ease-in-out;
        }
    }

    .navbar-text {
        transition: color 0.3s ease-in-out;
    }

    .navbar-item:hover .navbar-slashes {
        color: $color-black;
    }

    .navbar-item:hover {
        box-shadow: inset 100px 0 0 0 $color-white;
        color: $color-black;
    }
</style>

<main>
    <slot></slot>
</main>