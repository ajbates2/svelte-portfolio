<script>
  import TechBlock from "../../components/About/TechBlock.svelte";

  const about = `< About Me />`;
</script>

<section class="container">
  <TechBlock />
  <div class="bio">
    <h2>{about}</h2>
    <span>
      <p>
        Having worked in a restaurant and in the service industry for
        essentially my whole life, I work great in a team, and especially great
        in high stress situations. This has helped me greatly in my career as a
        software developer. Being able to communicate and stay calm no matter
        what the issue is that we are trying to resolve.
      </p>
      <p>
        My love for technology is what ultimately pushed me to get into web
        development. I love video games, movies, music, and Minnesota sports. I
        am a die hard Wolves and Vikings fan, at the expense of my own mental
        health. I have also played guitar my entire life, and love nerding out
        on everything involved with the instrument despite being not very good
        at it.
      </p>
    </span>
  </div>
</section>

<style>
  .container {
    display: grid;
    grid-gap: 20px;
    grid-template-columns: 1fr;
    grid-template-rows: 1fr auto;
    padding: 5vh 5vw;
    padding-top: 10vh;
    overflow-y: hidden;
  }

  .bio {
    padding: 36px;
    grid-column: 1;
    grid-row: 1;
    margin: 0;
    overflow-y: hidden;
    line-height: 45px;
    font-size: large;
    font-weight: 200;
    font-style: italic;
    display: grid;
    background-color: var(--glass-background);
    border-radius: 10px;
    box-shadow: -4px 20px 36px 8px var(--background);
  }

  h2 {
    color: var(--yellow);
    filter: drop-shadow(2px 1px 0px var(--background));
    font-style: italic;
    font-weight: 100;
    margin-top: 0;
    grid-row: 1;
    grid-column: 1;
  }

  span {
    grid-column: 1;
    grid-row: 2;
    place-self: center;
    margin: 16px;
  }

  @media only screen and (max-width: 650px) {
    .bio {
      font-size: medium;
      line-height: 35px;
      padding: 18px;
    }
    .container {
      height: inherit;
    }
  }
</style>
