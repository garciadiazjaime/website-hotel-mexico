<script>
  export let className
</script>

<style>
  div {
    position: relative;
  }

  .right-arrow:before, .left-arrow:before {
    content: '';
    width: 100%;
    background-color: var(--color-verde);
    height: 1px;
    top: 50%;
    display: block;
    position: absolute;
  }
  .right-arrow:before{
    right: 0;
  }
  .right-arrow:after {
    content: '';
    width: 7px;
    border-top: 1px solid var(--color-verde);
    border-right: 1px solid var(--color-verde);
    transform: rotate(45deg) translateY(-50%);
    height: 7px;
    top: 50%;
    display: block;
    right: 3px;
    position: absolute;
  }

  .left-arrow:before {
    right: -3px;
  }

  .left-arrow:after {
    content: '';
    width: 7px;
    border-top: 1px solid var(--color-verde);
    border-right: 1px solid var(--color-verde);
    transform: rotate(225deg) translateY(50%);
    height: 7px;
    top: 50%;
    display: block;
    left: 0px;
    position: absolute;
  }

  .white-arrow:before {
    border-top: 1px solid white;
    border-right: 1px solid white;
    height: 0;
  }
  .white-arrow:after {
    border-top: 1px solid white;
    border-right: 1px solid white;
  }
</style>

<div class={className}><slot></slot></div>
