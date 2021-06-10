<script>
  import { fade } from "svelte/transition"
</script>

<hr transition:fade={{ y: 200, duration: 1000 }} />

<style>
  hr {
    border-top: solid 5px var(--primary);
    padding-bottom: 0;
    margin-bottom: 3%;
  }
</style>
