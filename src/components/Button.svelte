<script>
  export let href
  export let target
  export let className
  export let onclick

</script>

<style>
  a {
    display: inline-block;
    color: white;
    background: var(--color-verde);
    text-decoration: none;
    text-transform: uppercase;
    position: relative;
    font-family: gotham;
    font-size: 14px;
    line-height: 14px;
  }
  .color-almendra {
    color: var(--color-almendra);
  }
  .small-arrow, .small-arrow-almendra {
    padding: 18px 42px 18px 20px;
  }
  .large-arrow {
    padding: 18px 120px 18px 20px;
    width: 100%;
    box-sizing: border-box;
  }

  .large-arrow:before {
    content: '';
    width: 60px;
    background-color: white;
    height: 1px;
    top: 23px;
    display: block;
    right: 20px;
    position: absolute;
  }
  .large-arrow:after, .small-arrow:after {
    content: '';
    width: 7px;
    border-top: 1px solid white;
    border-right: 1px solid white;
    transform: rotate(45deg) translateY(-50%);
    height: 7px;
    top: 23px;
    display: block;
    right: 23px;
    position: absolute;
  }

  .small-arrow-almendra:after {
    content: '';
    width: 7px;
    border-top: 1px solid var(--color-almendra);;
    border-right: 1px solid var(--color-almendra);;
    transform: rotate(45deg) translateY(-50%);
    height: 7px;
    top: 23px;
    display: block;
    right: 23px;
    position: absolute;
  }
</style>

<a on:click={onclick} class={className} href={href} target={target}><slot></slot></a>
