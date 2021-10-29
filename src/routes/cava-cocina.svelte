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
  h2 {
    color: goldenrod;
    text-transform: uppercase;
    font-size: 16px;
    text-align: center;
    margin-top: 60px;
  }
  .menu {
    text-align: center;
    text-transform: uppercase;
    position: relative;
    background:  radial-gradient(ellipse at center, transparent 0%, transparent 35%, gold 50%, transparent 50%);
    background-size: 15px 15px;
    background-repeat: repeat-x;
    background-position: 5px center;
  }
  .menu:after {
    content: "";
    width: 80px;
    height: 20px;
    display: block;
    margin: -20px auto 0;
    background: white;
  }
  h2 span {
    font-size: 10px;
    display: block;
  }
  .large-p {
    font-size: 22px;
    text-align: center;
    padding: 60px 150px 80px;
  }
  .dark {
    background-color: lightgray;
    padding: 80px 30px;
    box-sizing: border-box;
    position: relative;
    margin-bottom: 80px;
  }
  .dark:after {
    content: '';
    background:  radial-gradient(ellipse at center, transparent 0%, transparent 35%, gold 50%, transparent 50%);
    background-size: 15px 15px;
    background-repeat: repeat-x;
    background-position: 5px 0;
    width: 100%;
    height: 14px;
    border: none;
    position: absolute;
    bottom: -5px;
    left: 0;
  }
  ol {
    list-style-type: decimal-leading-zero;
    columns: 2;
    color: goldenrod;
    font-size: 30px;
    padding-left: 50px;
    margin: 0 20px 40px;
  }
  ol p {
    font-size: 14px;
    color: black;
    margin-top: 0;
    text-align: left;
  }
  .spec {
    text-transform: uppercase;
  }
  .banner-container {
    padding: 0 40px 80px;
    box-sizing: border-box;
  }
  .banner {
    background: goldenrod;
    padding: 30px 0;
    display: flex;
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
  h4, p {
    text-align: center;
  }
  h4 {
    color: goldenrod;
    font-size: 40px;
  }
  p span {
    text-transform: uppercase;
    display: block;
  }
</style>
<Header backgroundImage="https://picsum.photos/1000/400?random=16">
  <span slot="title">Lo mejor del valle<br>en nuestra cava</span>
</Header>
<h2><span>Hotel</span>Mexico en la piel</h2>
<p class='large-p'>
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
<div class="banner-container">
  <div class="banner">
    <img src="https://picsum.photos/100/100?random=12" alt="" />
    <p>Degusta en nuestra barra de vinos en grupo,<br>y conoce de la mejor calidad que tiene el Valle de Guadalupe</p>
    <a href="/reserva">Reserva ahora</a>
  </div>
</div>
<Header backgroundImage="https://picsum.photos/1000/400?random=4">
  <div slot="subheader">
    <Subheader color="white">Cocina</Subheader>
  </div>
  <span slot="title">
    Platillos y<br>aperitivos mexicanos
  </span>
  <div slot="icon">
    <img src="https://picsum.photos/100/100?random=15" alt="icon" />
  </div>
</Header>
<h3 class="menu">Menú</h3>
<h4>Aperitivos</h4>
<p>
  <span>Aperitivo No. 1</span>
  Texto descriptivo del aperitivo, información de la región
</p>
<p>
  <span>Aperitivo No. 2</span>
  Texto descriptivo del aperitivo, información de la región
</p>
<p>
  <span>Aperitivo No. 3</span>
  Texto descriptivo del aperitivo, información de la región
</p>
<h4>Especialidades</h4>
<p>
  <span>Platillo No. 1</span>
  Texto descriptivo del platillo, información de la región
</p>
<p>
  <span>Platillo No. 2</span>
  Texto descriptivo del platillo, información de la región
</p>
<p>
  <span>Platillo No. 3</span>
  Texto descriptivo del platillo, información de la región
</p>
<h4>Especialidades</h4>
<p>
  <span>Especialidad No. 1</span>
  Texto descriptivo del Especialidad, información de la región
</p>
<p>
  <span>Especialidad No. 2</span>
  Texto descriptivo del Especialidad, información de la región
</p>
<p>
  <span>Especialidad No. 3</span>
  Texto descriptivo del Especialidad, información de la región
</p>
<h2><span>Hotel</span>Mexico en la piel</h2>
