<script>
	import { onMount } from 'svelte';

	import Nav from '../components/Nav.svelte';
	import Button from '../components/Button.svelte'
	import Carousel from '../components/Carousel-Simple.svelte';

	let SvelteCarousel;
  onMount(async () => {
    const module = await import('svelte-carousel');
    SvelteCarousel = module.default;
  });

	const cabins = [
		{
			path: '/homepage/habitaciones/BajaCaliforniaSur.jpg',
			id: 'BajaCaliforniaSur',
			name: 'Baja California Sur',
		},
		{
			path: '/homepage/habitaciones/Chihuahua.jpeg',
			id: 'Chihuahua',
			name: 'Chihuahua',
		},
		{
			path: '/homepage/habitaciones/Coahuila.jpg',
			id: 'Coahuila',
			name: 'Coahuila',
		},
		{
			path: '/homepage/habitaciones/Durango.jpg',
			id: 'Durango',
			name: 'Durango',
		},
		{
			path: '/homepage/habitaciones/Sinaloa.jpg',
			id: 'Sinaloa',
			name: 'Sinaloa',
		},
		{
			path: '/homepage/habitaciones/Sonora.jpg',
			id: 'Sonora',
			name: 'Sonora',
		},
	];
	
	const slidesB = [
		{
			path: '/homepage/naturaleza/exterior_001.jpg',
			id: 'exterior_001',
		},
		{
			path: '/homepage/naturaleza/exterior_002.jpg',
			id: 'exterior_002',
		},
		{
			path: '/homepage/naturaleza/exterior_003.jpg',
			id: 'exterior_003',
		},
		{
			path: '/homepage/naturaleza/exterior_004.jpg',
			id: 'exterior_004',
		},
		{
			path: '/homepage/naturaleza/exterior_005.jpg',
			id: 'exterior_005',
		},
		{
			path: '/homepage/naturaleza/exterior_006.jpg',
			id: 'exterior_006',
		},
		{
			path: '/homepage/naturaleza/exterior_007.jpg',
			id: 'exterior_007',
		},
		{
			path: '/homepage/naturaleza/exterior_008.jpg',
			id: 'exterior_008',
		},
	]

	function arrowClickHandler(event, direction) {
		event.preventDefault()

		if (direction === 'left') {
			document.querySelector('.block-d .arrow-control-prev').click()
		} else {
			document.querySelector('.block-d .arrow-control-next').click()
		}
	}
</script>

<style>
	h1 {
		padding-left: 75px;
		font-family: mirage;
		font-weight: 200;
		font-size: 85px;
	}

	img {
		max-width: 100%;
		height: auto;
		display: block;
	}

	a {
		text-decoration: none;
	}

	p {
		margin: 0;
	}

	h1, h2, h3, ul {
		margin: 0;
	}

	ul {
		padding-left: 12px;
	}

	.content-menu {
		max-width: 1280px;
		margin: 0 auto;
		padding: 0 50px;
		box-sizing: border-box;
	}

	.content {
		max-width: 1280px;
		margin: 0 auto;
		padding: 0 140px;
		box-sizing: border-box;
	}
	
	.cover {
		position: relative;
		height: 100%;
	}

	.banner {
		background-image: url("/homepage/banner.jpg");
		height: 100%;
		background-position: center;
		background-repeat: no-repeat;
		background-size: cover;
	}

	.top {
		width: 100%;
		position: absolute;
		top: 0;
		left: 0;
		display: flex;
		justify-content: space-between;
		color: white;
		padding-top: 20px;
	}

	.title {
		position: absolute;
		top: 295px;
		font-size: 20px;
	}

	.title span {
		display: block;
		margin-left: 110px;
	}

	.header {
		display: flex;
		justify-content: space-between;
		align-items: baseline;
	}

	.header span {
		font-size: 12px;
		position: relative;
		top: 3px;
	}

	.header div {
		font-family: gotham;
	}

	.header h2 {
		font-family: trento;
		font-size: 4px;
	}

	.row {
		display: flex;
		justify-content: space-between;
	}

	.col-25 {
		width: 25%;
	}

	.col-40 {
		width: 40%;
	}

	.col-50 {
		width: 50%;
	}

	.col-58 {
		width: 58%;
	}

	.col-70 {
		width: 70%;
	}

	.col-75 {
		width: 75%;
	}

	.col-80 {
		width: 80%;
	}

	.col-100 {
		width: 100%;
	}

	.col-382 {
		width: 382px;
		vertical-align: top;
	}

	.padding-top-20 {
		padding-top: 20px;
	}

	.padding-top-30 {
		padding-top: 30px;
	}

	.padding-top-50 {
		padding-top: 50px;
	}

	.padding-top-60 {
		padding-top: 60px;
	}

	.padding-top-70 {
		padding-top: 70px;
	}

	.padding-top-80 {
		padding-top: 80px;
	}

	.padding-top-100 {
		padding-top: 100px;
	}

	.padding-top-150 {
		padding-top: 150px;
	}

	.padding-left-60 {
		padding-left: 60px;
	}

	h3 {
		font-size: 50px;
		color: var(--color-almendra);
		font-family: mirage;
		font-weight: 200;
		line-height: 50px;
	}

	h3 span {
		display: block;
		padding-left: 80px;
	}

	p {
		color: var(--color-verde);
		font-family: gotham;
	}

	p.strong {
		font-weight: 600;
	}

	.text-align-right {
		text-align: right;
	}

	.backgroun-light {
		background-color: var(--color-hueso);
	}

	.arrows {
		display: flex;
		justify-content: space-between;
		padding-top: 35px;
	}

	.position-relative {
		position: relative;
	}
	
	.over-image {
		width: 200px;
		position: absolute;
		top: -100px;
		right: 35px;
	}

	.text-center {
		text-align: center;
	}

	.block-center {
		margin: 0 auto;
	}

	.inline-block {
		display: inline-block;
	}

	.carousel {
		max-width: 585px;
	}

	.clear {
		clear: both;
	}

	.slide {
		position: relative;
	}

	.chevron-wrapper {
		background: url(/support/chevron.svg) repeat-x;
		height: 13px;
		margin: 0 auto;
		position: relative;
		top: 7px;
	}

	li {
		color: var(--color-almendra);
		font-family: gotham;
		font-size: 14px;
		margin: 6px 0 0;
	}

	.icon-b {
		width: 44px;
	}

	.brand {
		font-family: trento;
	}

	.signature {
		font-family: august;
		font-size: 80px;
		color: var(--color-almendra);
		position: relative;
		top: -20px;
	}


	.image-b-mask {
		max-height: 510px;
		overflow: hidden;
	}

	.pull-right {
		float: right;
	}

	.pull-left {
		float: left;
	}

	.arrow {
		width: 83px;
		height: 13px;
	}

	.arrow:hover {
		cursor: pointer;
	}

	.block-4-description {
		color: var(--color-almendra);
    display: block;
    width: 280px;
    padding-top: 50px;
	}

	.block-a {
		background-color: var(--color-hueso);
		padding-top: 150px;
	}

	.block-b {
		background-color: var(--color-hueso);
		padding-top: 200px;
	}

	.block-d {
		background-color: var(--color-verde);
		padding: 30px;
	}

	@media (min-width: 541px) and (max-width: 920px) {
		.content {
			padding: 0 12px;
		}
		.block-a {
			padding-top: 90px;
		}
		.block-a h3 span {
			padding-left: 20px;
		}
		.block-a .padding-top-80 {
			padding-top: 50px;
		}
		.col-382 {
			width: 200px;
		}
		.carousel {
			max-width: 520px;
		}

		.block-b {
			padding-top: 80px;
		}
		.image-b-mask {
			max-width: 45%;
			margin-right: 5%;
		}

		.block-d {
			padding: 12px;
			margin: 0 -12px;
		}
		.block-d .carousel {
			max-width: 450px;
		}
		.block-d .padding-left-60 {
			padding-left: 12px;
		}

		.block-e {
			padding-top: 100px;
		}
	}

	@media (max-width: 540px) {
		ul {
			margin-bottom: 200px;
		}
		h1 {
			padding-left: 20px;
			font-size: 40px;
		}
		h3 {
			margin-top: 20px;
			font-size: 42px;
		}
		h3 span {
			padding-left: initial;
			text-align: initial;
		}
		.content {
			padding: 12px;
		}
		.padding-left-60 {
			padding-left: 0;
		}
		.title span {
			margin-left: 20px;
		}
		.chevron-wrapper {
			width: 100%;
			top: 20px;
		}
		.brand {
			font-size: 10px;
		}
		.row {
			display: block;
		}
		.col-50 {
			width: auto;
		}
		.carousel {
			max-width: 100%;
		}
		.arrows {
			position: absolute;
			top: 0px;
			height: 100%;
			width: 100%;
		}
		.content-menu {
			padding: 0 12px;
		}
		.col-382 {
			width: 100%;
		}
		.pull-right {
			float: left;
		}
		.block-a { 
			padding-top: 40px;
		}
		.block-d {
			margin: 0 -12px;
			padding: 60px 12px 0;
		}
		.block-4-description {
			width: 100%;
		}
		.block-d .pull-right {
			width: 100%;
		}
		.block-e-description {
			width: 90%;
		}
	}
</style>

<svelte:head>
	<title>Sapper project template</title>
</svelte:head>


<div class="cover">
	<div class="banner"></div>
	<div class="top">
		<div class="content-menu col-100">
			<div class="header">
				<h2>HOTEL MÉXICO EN LA PIEL <span>®</span></h2>
				<div><a href="http://www.airbnb.com/p/hotelmexicoenlapiel" target="_blank">RESERVA</a></div>
			</div>

			<div class="title">
				<h1>Un homenaje <span>a nuestro México</span></h1>
			</div>
		</div>
	</div>
</div>


<Nav />

<div class="block-a">
	<div class="content">
		<div class="col-382 inline-block">
			<h3>Regresa <span>a casa</span></h3>
			<p class="padding-top-30 col-70">
				La calidez de nuestra tierra convertida en un espacio que te abraza, te da la bienvenida y parece que nunca se acaba.
			</p>
			<div class="padding-top-80">
				<Button href="/habitaciones" className="small-arrow">ver habitaciones</Button>
			</div>
			<div class="padding-top-50"></div>
		</div>

		<div class="carousel inline-block pull-right">
			<div class="slide">
				<Carousel slides={cabins} Carousel={SvelteCarousel} />
			</div>
		</div>
		<div class="clear"></div>
	</div>
</div>


<div class="block-b">
	<div class="content">
		<div class="row">
			<div class="image-b-mask">
				<img src="/homepage/copas_y_vino.jpg" alt="">
			</div>
			<div class="col-50">
				<h3>El Hotel de México, <span class="text-align-right">y el vino</span></h3>
				<p class="padding-top-50">Arquitectura que emerge de la tierra y se fusionan con su entorno, 13 “casas” que rinden homenaje a nuestro México, habitaciones con jacuzzi privado y una ubicación inigualable entre viñedos, áreas rocosas y un sorprendente bosque de encinos, distintas atmósferas dispuestas para emular de manera natural el territorio mexicano; una extensión de 15 hectáreas en donde espacios íntimos y de descanso convergen con espacios de celebración.</p>
				<br />
				<p class="col-75">Te invitamos a celebrar nuestra cultura y disfrutar de nuestra tierra.</p>
				<div class="padding-top-100">
					<Button href="http://www.airbnb.com/p/hotelmexicoenlapiel" className="large-arrow" target="_blank">reserva ahora</Button>
				</div>
			</div>
		</div>
	</div>
</div>


<div class="backgroun-light">
	<div class="padding-top-100"></div>
</div>

<div class="content padding-top-100">
	<h3 class="col-60">Despertar con todo <span>México ante tus ojos.</span></h3>

	<div class="row padding-top-70">
		<div class="col-50">
			<p class="col-80">Una experiencia exclusiva que le permitirá a cada uno de nuestros huéspedes explorar con todos sus sentidos los sabores de México, la riqueza de su tierra y sentir a flor de piel nuestra pasión por la cultura mexicana.</p>
			<br />
			<ul>
				<li>Espacios privados</li>
				<li>Casas con jacuzzi</li>
				<li>Servicio a cuarto</li>
				<li>Seguridad 24 hr</li>
				<li>Estacionamiento</li>
				<li>Transporte interno</li>
			</ul>
		</div>
		<div class="position-relative">
			<img class="over-image" src="/support/icon-a.svg" alt="">
			<img src="/homepage/info-hotel.jpg" alt="">
		</div>
	</div>
</div>


<div class="content">
	<div class="padding-top-100">
		<div class="chevron-wrapper"></div>
	</div>
</div>


<div class="backgroun-light padding-top-150">
	<div class="content">
		<div class="block-d">
			<div class="carousel inline-block pull-left">
				<div class="slide">
					<Carousel slides={slidesB} Carousel={SvelteCarousel} arrows={false} />
				</div>
			</div>

			<div class="padding-left-60 inline-block pull-right position-relative">
				<h3 class="padding-top-50">Naturaleza</h3>

				<p class="block-4-description">
					Paisajes que inspiran y nos llenan de orgullo; espacios naturales entre viñedos, vegetación endémica y encinares.
				</p>

				<img class="padding-top-50 icon-b" src="/support/icon-b.svg" alt="">

				<div class="padding-top-60">
					<div class="arrows">
						<div class="col-25">
							<a class="arrow" href="/" on:click={(event) => arrowClickHandler(event, 'left')}>
								<img src="/support/arrow-left-white.svg" alt="">
							</a>
						</div>
						<div class="col-25">
							<a class="arrow" href="/" on:click={event => arrowClickHandler(event, 'right')}>
								<img src="/support/arrow-right-white.svg" alt="">
							</a>
						</div>
					</div>
				</div>
			</div>

			<div class="clear"></div>
		</div>
	</div>
</div>


<div class="block-e backgroun-light">
	<div class="content padding-top-100 text-center">
		<p class="text-center strong">HOTEL</p>

		<div class="brand padding-top-30">México</div>
		<div class="signature">en la Piel</div>

		<p class="text-center strong">VALLE DE GUADALUPE</p>

		<br />

		<img class="block-center padding-top-20" src="/support/icon-c.png" alt="">

		<p class="block-e-description padding-top-50 col-58 block-center">
			Excelencia en cada detalle para que puedas disfrutar del Valle de Guadalupe en todas sus expresiones, desde su clima mediterráneo y sus paisajes espectaculares hasta el sabor de su comida y sus vinos más selectos.
		</p>
		<br />
		<p class="block-e-description text-center col-40 block-center">
			Una experiencia exclusiva y reconfortante, para celebrar el amor por México y el Valle de Guadalupe.
		</p>
	</div>
	<div class="padding-top-100"></div>
</div>
