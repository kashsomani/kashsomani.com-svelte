<script>
  import Details from './components/Details.svelte'
  import Navbar from "./components/Navbar.svelte"
  import Intro from "./components/Intro.svelte"
  import Matrix from "./components/Matrix.svelte"
// import Rain from "./components/Rain.svelte";
  let introRendered = false
</script>

<main>
  <Matrix/>
  <div class="px-8 lg:px-24 xl:px-32 pb-40 pt-8 md:pb-20">
    <!-- <Rain/> -->
    <Intro on:rendered={() => (introRendered = true)} />
    {#if introRendered}
      <Details/>
    {/if}
  </div>
  <div id="navbar">
    <Navbar />
  </div>
 
</main>

<style global lang="postcss">
  @tailwind base;
  @tailwind components;
  @tailwind utilities;
  #navbar{
    max-height: 17vh;
  }
</style>
