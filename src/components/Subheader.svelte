<script>
  export let color = 'black';
</script>
<style>
  h2 {
    text-transform: uppercase;
    font-size: 12px;
    font-family: sans-serif;
  }
  hr {
    margin: 10px 0 15px 50px;
    border: none;
    height: 1px;
  }
</style>
<div>
  <h2 style="color: {color}">
    <slot></slot>
  </h2>
  <hr class='hr'style="background-color: {color}">
</div>
