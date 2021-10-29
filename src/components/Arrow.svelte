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
    background-color: black;
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
    border-top: 1px solid black;
    border-right: 1px solid black;
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
    border-top: 1px solid black;
    border-right: 1px solid black;
    transform: rotate(225deg) translateY(50%);
    height: 7px;
    top: 50%;
    display: block;
    left: 0px;
    position: absolute;
  }
</style>

<div class={className}><slot></slot></div>
