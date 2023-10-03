<script>
  import Actions from "./Actions.svelte";
  import Icons from "./Icons.svelte";
</script>

<section class="container">
  <span>
    <h1 class="name">AJ Bates</h1>
    <h2 class="description">Full-Stack Developer</h2>
  </span>
  <Icons />
  <Actions />
</section>

<style>
  .container {
    grid-column: 1 / span 2;
    grid-row: 1;
    align-self: center;
    justify-self: center;
    z-index: 3;
    animation: FadeDown ease 2s;
    animation-iteration-count: 1;
    animation-fill-mode: forwards;
  }

  .name {
    font-size: 100px;
    font-style: italic;
    font-weight: 900;
    letter-spacing: -10px;
    margin: 0;
    filter: drop-shadow(17px 10px 25px var(--charcoal));
    color: var(--red);
  }

  .description {
    color: var(--yellow);
    filter: drop-shadow(2px 1px 0px var(--background));
    font-style: italic;
    font-weight: 100;
    margin-top: 0;
  }

  @media only screen and (max-width: 1000px) {
    .description {
      width: 75%;
    }
  }

  @media only screen and (max-width: 600px) {
    .container {
      grid-column: 1 / span 3;
      justify-self: center;
      align-self: center;
      text-align: center;
      padding-top: 30vh;
      background-color: rgb(68, 71, 90, 0.8);
      width: 100vw;
      height: inherit;
      backdrop-filter: blur(2px);
    }

    .description {
      width: 100%;
    }

    .name {
      font-size: 90px;
    }
  }
</style>
