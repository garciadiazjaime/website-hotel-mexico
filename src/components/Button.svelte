<script>
  export let href
  export let target
  export let className

</script>

<style>
  a {
    display: block;
    color: white;
    background: darkolivegreen;
    text-decoration: none;
    
    position: relative;
  }
  .small-arrow {
    text-transform: uppercase;
    padding: 18px 15px;
  }
  .large-arrow {
    padding: 10px 120px 10px 10px;
  }

  .large-arrow:before {
    content: '';
    width: 60px;
    background-color: white;
    height: 1px;
    top: 50%;
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
    top: 50%;
    display: block;
    right: 23px;
    position: absolute;
  }
</style>

<a class={className} href={href} target={target}><slot></slot></a>
