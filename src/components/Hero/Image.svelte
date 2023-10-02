<script>
  import transparent from "../../lib/images/transparent_headshot2.png";
</script>

<div class="container">
  <img
    class="headshot"
    src={transparent}
    alt="AJ looking to side and smiling"
  />
  <div class="blur" />
</div>

<style>
  .container {
    padding: 0;
    margin: 0;
    grid-column: 2 / span 3;
    grid-row: 1;
    justify-self: center;
    align-self: flex-end;
  }

  .headshot {
    filter: drop-shadow(-8px 0px 150px var(--charcoal));
    padding: 0;
    margin-bottom: -10px;
    max-height: 95vh;
    overflow-x: hidden;
    animation: FadeUp ease 1s;
    animation-iteration-count: 1;
    animation-fill-mode: forwards;
  }

  @media only screen and (max-width: 600px) {
    .headshot {
      height: 100vh;
    }
  }
</style>
