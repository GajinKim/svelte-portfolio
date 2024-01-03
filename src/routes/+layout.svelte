<script>
    import { base } from '$app/paths';
  </script>

<nav class="navbar">

    <div  class="navbar-left">
	    <a href="{base}/">Home</a>
    </div>

    <div class="navbar-right">
        <a href="{base}/about">About</a>
        <a href="{base}/settings">Settings</a>
        <a href="https://github.com/gajinkim">GitHub</a>
    </div>

</nav>

<style>
    .navbar {
        display: flex;
        justify-content: space-between;
    }

    .navbar-right {
        gap: 15px;
        display: flex;
        justify-content: flex-end;
    }

</style>

<main>
    <slot></slot>
</main>