<script>
  import { onMount } from "svelte";

  let menuOpen = false;

  function openMenu() {
    menuOpen = true;
  }

  function closeMenu() {
    menuOpen = false;
  }
</script>

<nav>
  <h3><span style="color: var(--secondary)">Ox</span><span style="color: var(--fg)">Qux</span></h3>

  <div class="links">
    <a href="#about">About</a>
    <a href="#portfolio">Portfolio</a>
    <a href="#experience">Experience</a>
    <a href="#contact">Contact</a>
  </div>

  <a class="burger" on:click={openMenu}>&#9776;</a>

  <div class="overlay {menuOpen ? 'active' : ''}" on:click={closeMenu}></div>

  <div class="mobile-menu {menuOpen ? 'active' : ''}" on:click={closeMenu}>
    <span class="close">×</span>
    <a href="#about">About</a>
    <a href="#portfolio">Portfolio</a>
    <a href="#experience">Experience</a>
    <a href="#contact">Contact</a>
  </div>
</nav>

<style>
  nav {
    top: 0;
    left: 0;
    width: 100%;
    position: fixed;
    display: flex;
    z-index: 1;
    padding: 0.1rem 1.2rem;
    align-items: center;
    box-sizing: border-box;
    justify-content: space-between;
    box-shadow: 0 4px 6px 2px rgba(0, 0, 0, 0.1);
    backdrop-filter: blur(2vh);
  }
  nav div {
    display: flex;
    gap: 1rem;
  }
  nav div a {
    padding: 0;
  }

  .burger {
    display: none;
  }
  .mobile-menu,
  .overlay {
    display: none;
  }
  @media (max-width: 768px) {
    .links {
      display: none;
    }

    .burger {
      display: block;
      font-size: 1.5rem;
      cursor: pointer;
    }
  }
  .mobile-menu {
    position: fixed;
    top: 0;
    right: -100%;
    width: 60%;
    height: 100vh;
    background: var(--bg);
    padding: 0.5rem 1.5rem;
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
    transition: 0.3s;
    z-index: 10;
  }
  .mobile-menu.active {
    right: 0;
  }
  .mobile-menu a {
    text-decoration: none;
    font-size: 1.2rem;
  }
  .close {
    font-size: 2rem;
    cursor: pointer;
    align-self: flex-end;
  }
  .overlay {
    position: fixed;
    height: 100vh;
    inset: 0;
    background: rgba(0,0,0,.5);
    z-index: 9;
  }
  .overlay.active {
    display: block;
  }
</style>
