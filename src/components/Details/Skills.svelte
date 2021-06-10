<script>
  import { fade } from "svelte/transition"
  import { icons } from "./skills-icons.js"
  $: borderActive = false
</script>

<div
  class="{borderActive
    ? 'detail-active'
    : ''} detail  px-4 text-primary py-8 text-center w-full"
  id="skills"
  transition:fade={{ y: 200, duration: 1000 }}
  on:introend={() => (borderActive = true)}
>
  <div class="detail-header">
    <h1 class="text-2xl font-semibold lg:text-4xl">Skills</h1>
  </div>
  <div class="p-4 w-full">
    <h1 class="text-base lg:text-lg xl:text-xl text-tertiary font-semibold p-2">
      PROGRAMMING LANGUAGES & TOOLS
    </h1>
    <p />

    <p />
    <div class="grid grid-cols-1 place-items-center p-0 w-full">
      <div class="grid grid-cols-3 place-items-center p-0 w-full">
        {#each icons as icon}
          <div class="w-24 grid grid-cols-1 items-center p-4 gap-2">
            <img src={icon.src} alt={icon.name} />
          </div>
        {/each}
      </div>
    </div>
  </div>
</div>
