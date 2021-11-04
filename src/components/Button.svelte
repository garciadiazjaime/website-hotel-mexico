<script>
  export let href
  export let target
  export let className

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
  .small-arrow {
    padding: 27px 54px 27px 20px;
  }
  .large-arrow {
    padding: 27px 120px 27px 20px;
    width: 100%;
    box-sizing: border-box;
  }

  .large-arrow:before {
    content: '';
    width: 60px;
    background-color: white;
    height: 1px;
    top: 32px;
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
    top: 32px;
    display: block;
    right: 23px;
    position: absolute;
  }
</style>

<a class={className} href={href} target={target}><slot></slot></a>
