<nav class="navbar">

    <div  class="navbar-left">
	    <a href="/">Home</a>
    </div>

    <div class="navbar-right">
        <a href="/about">About</a>
        <a href="/settings">Settings</a>
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

<body>
    <slot></slot>
</body>