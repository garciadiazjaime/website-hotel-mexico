<script>
  export let listItems = {};
  export let flexDirection = 'row';
  export let image = '';
  export let start = 1;
</script>
<style>
  div {
    display: flex;
  }
  ol {
    list-style-type: decimal-leading-zero;
    color: goldenrod;
    font-size: 30px;
  }
  ol p {
    font-size: 14px;
    color: black;
    margin-top: 0;
  }
  .spec {
    text-transform: uppercase;
  }

</style>
<div style="flex-direction: {flexDirection}">
  <ol start={start}>
    {#each listItems as item, i}
      <li>
        {item.nombre}
        <p class="spec">{item.varietal}<br>{item.year}</p>
        <p class="description">{item.descripcion}<br>{item.temperatura}</p>
      </li>
    {/each}
  </ol>
  <img src={image} alt="vinos" />
</div>
