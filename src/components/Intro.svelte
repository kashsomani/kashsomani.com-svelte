<script>
  import { onMount } from "svelte"
  import { createEventDispatcher } from "svelte"
  import { fly } from "svelte/transition"

  const dispatch = createEventDispatcher()
  onMount(() => (helloMounted = true))

  let helloMounted = false
  let kashSomani = false
  let webDeveloper = false
  let hackerman = false
  let active = false
</script>

<div class="p-6 {active ? 'shadow-in-plane active' : ''}" id="intro-container">
  {#if helloMounted}
    <div
      class="grid grid-cols-1 place-items-center text-primary text-4xl font-semibold text-center"
      transition:fly={{ y: 200, duration: 1200 }}
      on:introend={() => (kashSomani = true)}
    >
      Hello!
    </div>
  {/if}
  {#if kashSomani}
    <div
      class="grid grid-cols-1 place-items-center text-tertiary text-4xl text-center"
      transition:fly={{ y: 200, duration: 1500 }}
      on:introend={() => (webDeveloper = true)}
    >
      I'm Kash Somani
    </div>
  {/if}
  {#if webDeveloper}
    <div
      class="grid grid-cols-1 place-items-center text-primary text-4xl text-center"
      transition:fly={{ y: 200, duration: 2000 }}
      on:introend={() => (hackerman = true)}
    >
      and I am a Web Developer
    </div>
  {/if}
  {#if hackerman}
    <!-- dispatch('message', {
			text: 'Hello!'
		}); {helloMounted=false; kashSomani=false;webDeveloper=false;hackerman=false}} -->
    <div
      class="grid grid-cols-1 place-items-center text-primary text-xl text-center"
      transition:fly={{ y: 200, duration: 2000 }}
      on:introend={() => {
        dispatch("rendered")
        active = true
      }}
    >
      (basically hackerman)
    </div>
  {/if}
</div>

<style>
  #intro-container {
    background-color: transparent;
    height: 100%;
    border: 1px solid transparent;
    -webkit-transition: border 0.6s linear, box-shadow 0.6s linear, background 0.6s ease-in-out;
    -moz-transition: border 0.6s linear, box-shadow 0.6s linear;
    transition: border 0.6s linear, box-shadow 0.6s linear, background 0.6s ease-in-out;
  }
  #intro-container.active {
    background-color: var(--text-background);
    border-color: var(--tertiary);
    /* */
    
  }
</style>
