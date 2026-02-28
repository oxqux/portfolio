<script>
  import Nav from './navigation.svelte'

  import SectAbout from './sectionAbout.svelte'
  import SectPortf from './sectionPortfolio.svelte'
  import SectExp from './sectionExperience.svelte'
  import SectCont from './sectionContact.svelte'
</script>

<main>
 <Nav />
  <div class="indention"></div>
  <SectAbout />
  <div class="indention"></div>
  <SectPortf />
  <div class="indention"></div>
  <SectExp />
  <div class="indention"></div>
  <SectCont />
</main>

<style>
  .indention {
    padding: 5%;
    height: 20%;
  }
  @media (min-width: 768px) {
    .indention {
      padding: 5%;
      height: 5%;
    }
  }
</style>
