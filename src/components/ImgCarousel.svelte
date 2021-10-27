<script>
  import { fade } from 'svelte/transition';
  export let images = [];

  let index = 0;
  const next = () => {
    index = (index + 1) % images.length;
  }
  const prev = () => {
    index = (index - 1) % images.length;
  }
</script>
<style>
  img {
    width: 100%;
    position: absolute;
  }
  button {
    margin-top: 300px;
  }
</style>
{#each [images[index].path] as src (index)}
  <img transition:fade {src} alt="" />
{/each}
<button on:click={prev}>Prev</button>
<button on:click={next}>Next</button>
