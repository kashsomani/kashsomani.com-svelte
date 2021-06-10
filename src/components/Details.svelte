<script>
  import Experience from "./Details/Experience.svelte"
  import About from "./Details/About.svelte"
  import Education from "./Details/Education.svelte"
  import Skills from "./Details/Skills.svelte"
import Interests from "./Details/Interests.svelte"
</script>

<div class="pt-6">
  <div class="grid grid-rows-3 md:grid-flow-col gap-4">
    <div class="row-span-1"><About class="row-span-1" /></div>
    <div class="row-span-1"><Education class="row-span-1" /></div>
    <div class="row-span-1"><Skills class="row-span-1" /></div>
    <div class="row-span-2" id="Experience"><Experience /></div>
    <div class="row-span-1"><Interests /></div>

  </div>
</div>

<style>
</style>
