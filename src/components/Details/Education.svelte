<script>
  import { fade } from "svelte/transition"
  $: borderActive = false
</script>

<div
  class="{borderActive
    ? 'detail-active'
    : ''} detail  px-4 text-primary py-2 text-center grid grid-cols-1 place-items-center gap-0"
  transition:fade={{ y: 200, duration: 1000 }}
  on:introend={() => (borderActive = true)}
  id="education"
>
  <div class="detail-header w-full" >
    <h1 class="text-2xl font-semibold lg:text-4xl">Education</h1>
  </div>
  <div id="education-body p-0 m-0">
    <div class="p-4">
      <h1 class="text-base lg:text-lg  xl:text-2xl text-tertiary font-semibold">
        UNIVERSITY OF MASSACHUSETTS - AMHERST
      </h1>
      <p class="text-sm font-semibold lg:text-base xl:text-xl">
        BACHELOR OF SCIENCE IN <span class="text-tertiary"
          >COMPUTER SCIENCE</span
        >
        AND <span class="text-tertiary">MATHEMATICS</span>
      </p>
      <p class="text-lg lg:text-xl xl:text-2xl">Relavant Coursework</p>
      <div class="grid grid-cols-2 text-left gap-2 text-lg lg:text-xl xl:text-2xl">
        <p>
          <span class="text-tertiary">•</span> Machine Learning
        </p>
        <p>
          <span class="text-tertiary">•</span> Web Programming
        </p>
        <p>
          <span class="text-tertiary">•</span> Scalable Web Systems
        </p>
        <p>
          <span class="text-tertiary">•</span> Search Engines
        </p>
        <p>
          <span class="text-tertiary">•</span> Principles of Data Science
        </p>
        <p>
          <span class="text-tertiary">•</span> Algorithms
        </p>

        <p>
          <span class="text-tertiary">•</span> Advanced Calculus
        </p>
        <p>
          <span class="text-tertiary">•</span> Statistics I & II
        </p>
        <p>
          <span class="text-tertiary">•</span> Abstract Algebra
        </p>
      </div>
    </div>
  </div>
</div>

<style>

</style>