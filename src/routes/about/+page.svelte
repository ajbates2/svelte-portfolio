<script>
  import TechBlock from "../../components/About/TechBlock.svelte";
</script>

<section class="container">
  <TechBlock />
  <div class="bio">
    <p>
      Having worked in a restaurant and in the service industry for essentially
      my whole life, I work great in a team, and especially great in high stress
      situations. I can't wait to work with a great team of programmers and
      developers to apply my knowledge to a different challenge everyday.
    </p>
    <p>
      My love for technology is what ultimately pushed me to get into web
      development. I enjoy video games (built multiple PC's), movies, and music.
      When I'm not coding you might find me bartending (I love beer), or going
      to see some live music (whenever we're allowed). Just like every other
      millennial I collect vinyl and shoes.
    </p>
  </div>
</section>

<style>
  .container {
    padding: 10vh 0;
    display: grid;
    grid-template-columns: 40vw auto;
    grid-gap: 20px;
    height: 100vh;
  }

  .bio {
    padding: 10%;
    grid-column: 2;
    margin-right: 4vw;
    line-height: 45px;
    font-size: large;
    font-weight: 200;
    font-style: italic;
    display: grid;
    place-items: center;
    background-color: var(--glass-background);
    border-radius: 10px;
    box-shadow: -4px 20px 36px 8px var(--background);
    animation: FadeUp ease 2s;
    animation-iteration-count: 1;
    animation-fill-mode: forwards;
  }

  @media only screen and (max-width: 900px) {
    .container {
      grid-template-columns: 1fr;
      grid-template-rows: 1fr auto;
      padding: 5vh 5vw;
      padding-top: 10vh;
      height: inherit;
    }

    .bio {
      grid-row: 1;
      grid-column: 1;
      margin: 0;
    }
  }

  @media only screen and (max-width: 650px) {
    .bio {
      font-size: medium;
      line-height: 35px;
    }
    .container {
      height: inherit;
    }
  }
</style>
