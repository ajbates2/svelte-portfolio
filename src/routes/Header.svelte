<script>
  import { page } from "$app/stores";
</script>

<header>
  <nav>
    <ul>
      <li aria-current={$page.url.pathname === "/" ? "page" : undefined}>
        <a href="/">Home</a>
      </li>
      <li aria-current={$page.url.pathname === "/about" ? "page" : undefined}>
        <a href="/about">About</a>
      </li>
      <!-- <li
        aria-current={$page.url.pathname === "/projects" ? "page" : undefined}
      >
        <a href="/projects">projects</a>
      </li> -->
      <li aria-current={$page.url.pathname === "/contact" ? "page" : undefined}>
        <a href="/contact">contact</a>
      </li>
    </ul>
  </nav>
</header>

<style>
  header {
    position: absolute;
    top: 0;
    z-index: 10;
    width: 100%;
    display: flex;
    justify-content: center;
    background: transparent;
    animation: FadeDown ease 2s;
    animation-iteration-count: 1;
    animation-fill-mode: forwards;
  }

  ul {
    display: flex;
    justify-content: center;
    align-items: center;
    list-style: none;
  }

  li {
    position: relative;
    height: 100%;
  }

  li[aria-current="page"] a {
    color: var(--red);
  }

  nav a {
    display: flex;
    height: 100%;
    align-items: center;
    padding: 0 0.5rem;
    color: var(--foreground);
    font-weight: 700;
    font-size: 0.8rem;
    text-transform: uppercase;
    letter-spacing: 0.1em;
    text-decoration: none;
    transition: color 0.2s linear;
  }

  a:hover {
    color: var(--cyan);
  }
</style>
