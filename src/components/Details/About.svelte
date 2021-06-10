<script>
  import { fade } from "svelte/transition"
  import {links} from './links.js'
  $: borderActive = false
</script>

<div
  class="{borderActive ? 'detail-active' : ''} detail px-4 text-primary py-8 text-center "
  id="about"
  transition:fade={{ y: 200, duration: 1000 }}
  on:introend={() => (borderActive = true)}
>
  <div class="detail-header">
    <h1 class="text-2xl font-semibold lg:text-4xl">About Me</h1>
  </div>
  <div class="grid grid-cols-1 place-items-center gap-0 h-5/6 text-lg xl:text-2xl">
    <div >
      <div class="p-4 text-justify-last ">
        <p>
          Did you ever go through a phase as a kid where you loved solving riddles?
          You would constantly try to find new ones you can solve, and you probably
          remember how fun that was. Or maybe still is. I take the same amount of
          joy in Software | Web development as you may take in solving riddles.
        </p>
    
        <p>And here are some words | numbers:</p>
        <p>
          B.S in Computer Science and Mathematics, University of Massachusetts,
          Amherst - 2021 GPA: 3.72
        </p>
      </div>
      <div class="grid grid-cols-3 place-items-center p-0">
        {#each links as link}
        <div class="w-24 grid grid-cols-1 items-center p-2">
          <a href="{link.link}"><img src="{link.src}" alt="{link.name}" ></a>
        </div>
        {/each}
      </div>
    </div>
    
    </div>
  </div>
  
