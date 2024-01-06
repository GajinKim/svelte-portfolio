<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Poppins:wght@100;200;300;400;500;600;700;800;900&family=Work+Sans:wght@100;200;300;400;500;600;700;800;900&display=swap">


<style lang="scss">
    $color-black: #100c08;
    $color-white: #f4f3d7;
    $color-beige: #ecc298;

    main {
        font-family: "Poppins", sans-serif;
        text-align: left;
        /* padding-left: max(5px, 20vw);
        padding-right: max(5px, 20vw); */
        height: 1500px;
        background-color: $color-beige;
        /* position: absolute; */
    }

    .about-content {

        font-size:  clamp(10px, 1.5vw, 20px);
        color: $color-black;

        padding-top: max(50px, 10vh);
        padding-bottom: max(50px, 10vh);

        // deadspace padding for desktop users
        @media (pointer:fine) {
            padding-left: 30vw;
            padding-right: 30vw;
        }
    }
</style>

<main>
    <p class="about-content">
        // todo, make this less cringe

        <br>

        
        Software Consultant at Source Allies with 4+ years of experience. <br/>
        Specializing in <span class="aws-subtitle">AWS Cloud Architecture</span>, let's turn <b>bold ideas</b> into <b>reality</b>!
    </p>
</main>