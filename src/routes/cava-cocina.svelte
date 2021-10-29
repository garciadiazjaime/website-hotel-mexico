<script>
  import Header from '../components/Header.svelte';
  import Subheader from '../components/Subheader.svelte';
  import ListWithImage from '../components/ListWithImage.svelte';
  const vinos = [
    {
      nombre: 'Monte Xanic',
      varietal: '100% sauvignon blanc',
      year: '2019',
      descripcion: 'Fermentación elaborada en tanques de acero inoxidable a temperatura controlada entre',
      temperatura: '13 - 15 °C',
    },
    {
      nombre: 'L.A. Cetto',
      varietal: '100% Merlot',
      year: '2017',
      descripcion: 'Fermantación elabaroda en tanques de acero inoxidable a temperatura controlada entre',
      temperatura: '13 - 15  ̊C',
    },
    {
      nombre: 'Roganto',
      varietal: '100% Nebbiolo',
      year: '2014',
      descripcion: 'Fermantación elabaroda en tanques de acero inoxidable a temperatura controlada entre',
      temperatura: '13 - 15  ̊C',
    },
    {
      nombre: 'Las Nubes',
      varietal: '100% SAUVIGNON BLANC',
      year: '2019',
      descripcion: 'Fermantación elabaroda en tanques de acero inoxidable a temperatura controlada entre',
      temperatura: '13 - 15  ̊C',
    },
    {
      nombre: 'Casa Madero',
      varietal: '100% Merlot',
      year: '2017',
      descripcion: 'Fermantación elabaroda en tanques de acero inoxidable a temperatura controlada entre',
      temperatura: '13 - 15  ̊C',
    },
    {
      nombre: 'Don Luis (L.A. Cetto)',
      varietal: '100% Nebbiolo',
      year: '2014',
      descripcion: 'Fermantación elabaroda en tanques de acero inoxidable a temperatura controlada entre',
      temperatura: '13 - 15  ̊C',
    },
    {
      nombre: 'Gran Ricardo',
      varietal: '100% SAUVIGNON BLANC',
      year: '2019',
      descripcion: 'Fermantación elabaroda en tanques de acero inoxidable a temperatura controlada entre',
      temperatura: '13 - 15  ̊C',
    },
    {
      nombre: 'Casa Magoni',
      varietal: '100% Merlot',
      year: '2017',
      descripcion: 'Fermantación elabaroda en tanques de acero inoxidable a temperatura controlada entre',
      temperatura: '13 - 15  ̊C',
    },
    {
      nombre: 'Emeve',
      varietal: '100% SAUVIGNON BLANC',
      year: '2019',
      descripcion: 'Fermantación elabaroda en tanques de acero inoxidable a temperatura controlada entre',
      temperatura: '13 - 15  ̊C',
    },
    {
      nombre: 'Casa de Piedra',
      varietal: '100% Merlot',
      year: '2017',
      descripcion: 'Fermantación elabaroda en tanques de acero inoxidable a temperatura controlada entre',
      temperatura: '13 - 15  ̊C',
    },
  ]
</script>
<style>
  div {
    width: 100%;
  }
  .dark {
    background-color: lightgray;
    padding: 80px 30px;
    box-sizing: border-box;
    position: relative;
  }
  .dark:after {
    content: '';
    background:  radial-gradient(ellipse at center, transparent 0%, transparent 35%, gold 50%, transparent 50%);
    background-size: 15px 15px;
    background-repeat: repeat-x;
    background-position: 5px center;
    width: 100vw;
    height: 12px;
    border: none;
    position: absolute;
    bottom: -6px;
    width: 100%;
  }
  ol {
    list-style-type: decimal-leading-zero;
    columns: 2;
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
  .banner {
    background: goldenrod;
    padding: 30px 0;
    display: flex;
    margin: 0 40px 80px;
    justify-content: space-between;
    flex-direction: column;
    align-items: center;
    box-sizing: border-box;
  }
  .banner a {
    text-decoration: none;
    position: relative;
    padding-right: 90px;

  }
  .banner a:before {
    content: '';
    width: 60px;
    background-color: black;
    height: 1px;
    top: 50%;
    display: block;
    right: 20px;
    position: absolute;
  }
  .banner a:after {
    content: '';
    width: 5px;
    border-top: 1px solid black;
    border-right: 1px solid black;
    transform: rotate(45deg) translateY(-50%);
    height: 5px;
    top: 50%;
    display: block;
    right: 23px;
    position: absolute;
  }
</style>
<Header backgroundImage="https://picsum.photos/1000/400?random=16">
  <span slot="title">Lo mejor del valle<br>en nuestra cava</span>
</Header>
<h2><span>Hotel</span>Mexico en la piel</h2>
<p>
  Encontramos en la calidez de nuestra tierra, el encantode sus paisajes y el sabor de cada uno de nuestros recuerdos, inspiración para crear texturas y emociones que nos transporten a nuestros orígenes, pero sobre todo nos permitan disfrutar la vida al máximo.
</p>
<Header backgroundImage="https://picsum.photos/1000/400?random=1">
  <div slot="subheader">
    <Subheader color="white">Cava</Subheader>
  </div>
  <span slot="title">
    Nuestros 10 vinos<br>seleccionados del Valle
  </span>
  <div slot="icon">
    <img src="https://picsum.photos/100/100?random=16" alt="icon" />
  </div>
</Header>
<div class="dark">
  <ListWithImage
    listItems={vinos.slice(0,3)}
    image="https://picsum.photos/300/500?random=14"
  ></ListWithImage>
  <ListWithImage
    listItems={vinos.slice(3,6)}
    image="https://picsum.photos/300/500?random=15"
    flexDirection="row-reverse"
    start="4"
  ></ListWithImage>
</div>
<ol start="7">
  {#each vinos.slice(6) as item, i}
    <li>
      {item.nombre}
      <p class="spec">{item.varietal}<br>{item.ano}</p>
      <p class="description">{item.descripcion}<br>{item.temperatura}</p>
    </li>
  {/each}
</ol>
<div class="banner">
  <img src="https://picsum.photos/100/100?random=12" alt="" />
  <p>Degusta en nuestra barra de vinos en grupo,<br>y conoce de la mejor calidad que tiene el Valle de Guadalupe</p>
  <a href="/reserva">Reserva ahora</a>
</div>
