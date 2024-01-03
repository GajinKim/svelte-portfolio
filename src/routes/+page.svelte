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

    
.aws-subtitle {
    font-size:  clamp(20px, 6vw, 40px);
    line-height: clamp(20px, 6vw, 40px);
    text-shadow: 0 0 5px #FF9900, 0 0 15px #FF9900, 0 0 20px #FF9900, 0 0 40px #FF9900, 0 0 60px #ff0000, 0 0 10px #ff8d00, 0 0 98px #ff0000;
    color: #fff6a9;
    text-align: center;
    animation: blink 12s infinite;
    -webkit-animation: blink 12s infinite;
}

@-webkit-keyframes blink {
  20%,
  24%,
  55% {
    color: #111;
    text-shadow: none;
  }

  0%,
  19%,
  21%,
  23%,
  25%,
  54%,
  56%,
  100% {

  text-shadow: 0 0 5px #FF9900, 0 0 15px #FF9900, 0 0 20px #FF9900, 0 0 40px #FF9900, 0 0 60px #ff0000, 0 0 10px #ff8d00, 0 0 98px #ff0000;
    color: #fff6a9;
  }
}

@keyframes blink {
  20%,
  24%,
  55% {
    color: #111;
    text-shadow: none;
  }

  0%,
  19%,
  21%,
  23%,
  25%,
  54%,
  56%,
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
    <p class="name">Gajin Kim</p>
    <p class="subtitle" ><span class="aws-subtitle">AWS Cloud</span> Enthusiast</p>
</main>