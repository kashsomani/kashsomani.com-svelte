<script>
  import * as animateScroll from "svelte-scrollto"
</script>

<nav class="p-3 md:p-1 navbar-color fixed shadow-lg bottom-0 w-screen">
  <div
    class="grid grid-flow-col grid-cols-1 grid-rows-2 md:grid-cols-2 md:grid-rows-1"
  >
    <div
      class="sm:flex text-primary flex items-center justify-center md:items-start md:justify-start"
    >
      <a href="#" class="text-3xl font-bold p-3">
        <span class="logo-container">KS</span>
      </a>
    </div>

    <div class=" flex items-center justify-center text-primary">
      <table class="buttons text-base xl:text-lg">
        <tr>
          <td
            ><button
              type="button"
              on:click={() =>
                animateScroll.scrollTo({
                  element: "#about",
                })}>About</button
            >
          </td><td
            ><button
              type="button"
              on:click={() =>
                animateScroll.scrollTo({
                  element: "#experience",
                })}>Experience</button
            >
          </td><td
            ><button
              type="button"
              on:click={() =>
                animateScroll.scrollTo({
                  element: "#education",
                })}>Education</button
            >
          </td><td
            ><button
              type="button"
              on:click={() =>
                animateScroll.scrollTo({
                  element: "#skills",
                })}>Skills</button
            >
          </td><td
            ><button
              type="button"
              on:click={() =>
                animateScroll.scrollTo({
                  element: "#interests",
                })}>Interests</button
            >
          </td></tr
        >
      </table>
    </div>
  </div>
</nav>

<style>
  nav {
    border-top: 4px solid var(--tertiary);
  }
  .buttons {
    width: 95%;
    table-layout: fixed;
    border-collapse: collapse;
  }
  .buttons button {
    width: 100%;
    border: 2px solid;
    border-radius: 10%;
    border-color: var(--primary);
    text-overflow: ellipsis;
    overflow: hidden;
    outline: none;
  }
  .buttons button:hover {
    cursor: url("../assets/cursor2.png"), default;
    box-shadow: 0px 16px 24px 2px rgba(19, 255, 198, 0.14),
      0px 6px 30px 5px rgba(19, 255, 198, 0.12),
      0px 8px 10px -7px rgba(19, 255, 198, 0.2);
    background-color: var(--tertiary);
    border-color: var(--tertiary);
    color: var(--dark);
  }
  .logo-container {
    border: 0.3rem solid;
    padding: 0.2rem;
    border-color: var(--primary);
    box-shadow: 0.25rem 0.25rem rgba(32, 173, 182, 0.8);
  }
  .logo-container:hover {
    color: var(--tertiary);
    cursor: url("../assets/cursor2.png"), default;
    box-shadow: 0.25rem 0.25rem rgba(19, 255, 198, 0.8),
      rgba(19, 255, 198, 0.8) 0rem 0.44rem 1.4rem 0.08rem;
  }
</style>
