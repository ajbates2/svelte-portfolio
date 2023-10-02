<script>
  import ReactIcon from "~icons/logos/react";
  import NodeIcon from "~icons/logos/nodejs-icon";
  import VueIcon from "~icons/logos/vue";
  import ViteIcon from "~icons/logos/vitejs";
  import ExpressIcon from "~icons/simple-icons/express";
  import ExpoIcon from "~icons/logos/expo-icon";
  import GitHubIcon from "~icons/logos/github-icon";
  import GitIcon from "~icons/logos/git-icon";
  import GunIcon from "~icons/logos/gunjs";
  import SvelteIcon from "~icons/logos/svelte-icon";
  import AzureIcon from "~icons/logos/azure-icon";
  import PostgresIcon from "~icons/logos/postgresql";
</script>

<div class="container">
  <div class="icon_pair">
    <span>
      <ReactIcon />
    </span>
    <aside>React</aside>
  </div>
  <div class="icon_pair">
    <span>
      <VueIcon />
    </span>
    <aside>Vue</aside>
  </div>
  <div class="icon_pair">
    <span>
      <SvelteIcon />
    </span>
    <aside>Svelte</aside>
  </div>
  <div class="icon_pair">
    <span>
      <GunIcon />
    </span>
    <aside>Gun.js</aside>
  </div>
  <div class="icon_pair">
    <span>
      <ViteIcon />
    </span>
    <aside>Vite</aside>
  </div>
  <div class="icon_pair">
    <span>
      <ExpoIcon />
    </span>
    <aside>Expo</aside>
  </div>
  <div class="icon_pair">
    <span>
      <NodeIcon />
    </span>
    <aside>Node.js</aside>
  </div>
  <div class="icon_pair">
    <span>
      <ExpressIcon />
    </span>
    <aside>Express.js</aside>
  </div>
  <div class="icon_pair">
    <span>
      <PostgresIcon />
    </span>
    <aside>Postgresql</aside>
  </div>
  <div class="icon_pair">
    <span>
      <GitIcon />
    </span>
    <aside>Git</aside>
  </div>
  <div class="icon_pair">
    <span>
      <GitHubIcon />
    </span>
    <aside>GitHub</aside>
  </div>
  <div class="icon_pair">
    <span>
      <AzureIcon />
    </span>
    <aside>Azure</aside>
  </div>
</div>

<style>
  .container {
    padding: 5%;
    grid-column: 1;
    margin-left: 4vw;
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    background-color: var(--glass-background);
    border-radius: 10px;
    box-shadow: -4px 20px 36px 8px var(--background);
    animation: FadeUp ease 2s;
    animation-iteration-count: 1;
    animation-fill-mode: forwards;
  }

  .icon_pair {
    text-align: center;
    margin: 30px;
  }

  .icon_pair span {
    display: block;
    font-size: 60px;
    filter: drop-shadow(2px 2px 3px var(--background));
    transition: all 0.2s ease-out;
  }

  .icon_pair span:hover {
    transform: translateY(-2px);
    filter: drop-shadow(2px 4px 3px var(--charcoal));
  }

  .icon_pair aside {
    font-size: 12px;
    font-weight: 100;
    font-style: italic;
  }

  @media only screen and (max-width: 900px) {
    .icon_pair span {
      font-size: 45px;
    }
  }

  @media only screen and (max-width: 1100px) {
    .container {
      grid-template-columns: 1fr 1fr;
    }
  }

  @media only screen and (max-width: 900px) {
    .container {
      grid-row: 2;
      margin: 0;
      grid-template-columns: 1fr 1fr 1fr;
    }

    .icon_pair span {
      font-size: 45px;
    }
  }

  @media only screen and (max-width: 400px) {
    .container {
      grid-template-columns: 1fr 1fr;
    }
  }
</style>
