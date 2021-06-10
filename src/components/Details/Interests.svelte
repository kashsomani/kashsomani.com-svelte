<script>
  import { fade } from "svelte/transition"
  $: borderActive = false
</script>

<div
  class="{borderActive
    ? 'detail-active'
    : ''} detail px-4 text-primary py-8 text-center"
  id="interests"
  transition:fade={{ y: 200, duration: 1000 }}
  on:introend={() => (borderActive = true)}
>
  <div class="detail-header">
    <h1 class="text-2xl lg:text-4xl font-semibold">INTERESTS</h1>
  </div>
  <div class="grid grid-cols-1 place-items-center gap-0 h-5/6 text-lg lg:text-2xl">
    <div>
      <div class="p-4 text-justify-last">
        <p>
          Apart from being a web developer, I enjoy most of my time playing
          chess, playing social deception games with my friends. Strumming my
          guitar on a warm sunny day at the beach is my ideal Sunday
        </p>

        <p>
          I also do enjoy playing a lot of board games and sketching, and I
          spend a large amount of my free time exploring the latest technology
          advancements in the web development world.
        </p>
      </div>
    </div>
  </div>
</div>
