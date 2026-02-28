<section id="portfolio">
  <h2>Portfolio</h2>
  <div class="projects">
    <div class="projectCard">
      <img src="./portfolio/calculator.png" />
      <div>
        <h3>Calculator</h3>
        <p>
          A lightweight, extensible calculator built with pure <b>HTML</b>,
          <b>CSS</b>, and <b>JavaScript</b>. It supports a plugin system for
          customization and new functionality, includes light and dark themes,
          and runs entirely in the browser without external frameworks.
        </p>
        <a href="https://github.com/oxqux/Calculator">Read more</a>
      </div>
    </div>

    <div class="projectCard">
      <img src="./portfolio/notedo.png" />
      <div>
        <h3>NoteDo</h3>
        <p>
          A simple note-taking app built with <b>React</b> and
          <b>React Router</b>. Create notes, edit them in <b>Markdown</b>,
          rename, delete and manage everything locally. No backend. No accounts.
          No sync. Just notes sitting in your browser like they should.
        </p>
        <a href="https://github.com/oxqux/NoteDo">Read more</a>
      </div>
    </div>

    <div class="projectCard">
      <img src="./portfolio/quotedrip.png" />
      <div>
        <h3>QuoteDrip</h3>
        <p>
          <b>QuoteDrip</b> is a sleek, modern random quote generator built with a
          focus on minimalist design and a seamless user experience. Designed to inspire,
          it fetches curated quotes from around the world in their original languages.
        </p>
        <a href="https://github.com/oxqux/QuoteDrip">Read more</a>
      </div>
    </div>
  </div>
  <a href="https://github.com/oxqux" target="_blank" rel="noopener"
    ><button>GitHub repository</button></a
  >
</section>

<style>
  .projects {
    display: grid;
    gap: 1rem;
  }
  .projectCard {
    display: flex;
    flex-direction: column;
    text-align: left;
    padding: 1.5rem;
    margin: 0;
    justify-content: space-around;
    align-items: center;
    border-radius: 1.5rem;
    box-shadow: 2px 2px 10px black;
  }
  .projectCard div {
    text-align: left;
  }
  .projectCard img {
    width: 100%;
    height: auto;
    max-width: 300px;
    border-radius: 1rem;
  }
  h3 {
    font-size: 2rem;
    margin: 0.2rem;
  }
  button {
    margin-top: 10%;
  }

  @media (min-width: 768px) {
    .projectCard {
      flex-direction: row;
      margin: 0 4rem;
    }

    .projectCard img {
      width: auto;
      height: 10rem;
      max-width: none;
    }
    .projectCard div {
      margin-left: 1.5rem;
    }
  }
</style>
