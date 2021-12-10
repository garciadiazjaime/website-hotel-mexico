<script>
  import { onMount } from 'svelte';

  const text = 'C%C3%B3modas%20habitaciones%20te%20dar%C3%A1n%20la%20bienvenida%2C%20amenidades%20de%20lujo%20y%20un%20staff...'
  let showSocialMedia = false

  function clickHandlerShare(event) {
    event.preventDefault()
    showSocialMedia = !showSocialMedia
  }

  onMount(async () => {
    document.body.addEventListener('click', (event) => {
      if (event.target && !event.target.classList.contains('share') && showSocialMedia) {
        showSocialMedia = false
      }
    }); 
  });
</script>
<style>
  .share {
    background-color: var(--color-almendra);
    width: 75px;
    height: 26px;
    box-sizing: border-box;
    display: block;
    float: right;
    color: white;
    padding: 4px 7px;
    text-decoration: none;
    border-radius: 5px;
    position: relative;
  }
  .share:hover {
    cursor: pointer;
  }
  .share:after {
    content: '';
    width: 7px;
    border-top: 1px solid white;
    border-right: 1px solid white;
    transform: rotate(45deg) translateY(-50%);
    height: 7px;
    top: 46%;
    display: block;
    right: 14px;
    position: absolute;
  }
  .logos {
    position: absolute;
    top: -28px;
    right: -55px;
    z-index: 1;
  }
  .facebook {
    background-color: #3b5998;
    fill: #fff;
    stroke: none;
    padding: 0.75em;
    display: flex;
  }
  .twitter {
    background-color:#55acee;
    fill: #fff;
    stroke: none;
    padding: 0.75em;
    display: flex;
  }
  svg {
    width: 20px;
    height: 20px;
  }
  @media (max-width: 1080px) {
    .share {
      float: none;
    }
    .logos {
      top: 0;
      left: 85px;
      right: initial;
    }
  }
</style>

<a href="/" class="share" on:click={clickHandlerShare}>Share</a>

{#if showSocialMedia}
  <div class="logos">
    <a href="https://facebook.com/sharer/sharer.php?u=https://hotelmexicoenlapiel.com/habitaciones" target="_blank" rel="noopener" aria-label="Share on Facebook">
      <div class="facebook">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M18.77 7.46H14.5v-1.9c0-.9.6-1.1 1-1.1h3V.5h-4.33C10.24.5 9.5 3.44 9.5 5.32v2.15h-3v4h3v12h5v-12h3.85l.42-4z"></path></svg>
      </div>
    </a>
    <a href="https://twitter.com/intent/tweet/?text={text}&amp;hashtags=&amp;via=&amp;related=&amp;url=https://hotelmexicoenlapiel.com/habitaciones" target="_blank" rel="noopener" aria-label="Share on Twitter">
      <div class="twitter">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24"><path d="M23.44 4.83c-.8.37-1.5.38-2.22.02.93-.56.98-.96 1.32-2.02-.88.52-1.86.9-2.9 1.1-.82-.88-2-1.43-3.3-1.43-2.5 0-4.55 2.04-4.55 4.54 0 .36.03.7.1 1.04-3.77-.2-7.12-2-9.36-4.75-.4.67-.6 1.45-.6 2.3 0 1.56.8 2.95 2 3.77-.74-.03-1.44-.23-2.05-.57v.06c0 2.2 1.56 4.03 3.64 4.44-.67.2-1.37.2-2.06.08.58 1.8 2.26 3.12 4.25 3.16C5.78 18.1 3.37 18.74 1 18.46c2 1.3 4.4 2.04 6.97 2.04 8.35 0 12.92-6.92 12.92-12.93 0-.2 0-.4-.02-.6.9-.63 1.96-1.22 2.56-2.14z"></path></svg>
      </div>
    </a>
  </div>
{/if}
