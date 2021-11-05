<script>
	import Nav from '../components/Nav.svelte';
	import Button from '../components/Button.svelte'
	import Arrow from '../components/Arrow.svelte'
</script>

<style>
	@font-face {
		font-family: "mirage";
		src: url("/fonts/mirage/mirage-thin.otf");
		font-weight: 100;
		font-style: normal;
	}
	@font-face {
		font-family: "mirage";
		src: url("/fonts/mirage/mirage-regular.otf");
		font-weight: 200;
		font-style: normal;
	}
	@font-face {
		font-family: "mirage";
		src: url("/fonts/mirage/mirage-medium.otf");
		font-weight: 400;
		font-style: normal;
	}
	@font-face {
		font-family: "mirage";
		src: url("/fonts/mirage/mirage-bold.otf");
		font-weight: 600;
		font-style: normal;
	}
	@font-face {
		font-family: "mirage";
		src: url("/fonts/mirage/mirage-black.otf");
		font-weight: 800;
		font-style: normal;
	}


	@font-face {
		font-family: "gotham";
		src: url("/fonts/gotham/Gotham-XLight.ttf");
		font-weight: 100;
		font-style: normal;
	}
	@font-face {
		font-family: "gotham";
		src: url("/fonts/gotham/Gotham-XLightItalic.ttf");
		font-weight: 100;
		font-style: italic;
	}
	@font-face {
		font-family: "gotham";
		src: url("/fonts/gotham/Gotham-Medium.ttf");
		font-weight: 200;
		font-style: normal;
	}
	@font-face {
		font-family: "gotham";
		src: url("/fonts/gotham/Gotham-MediumItalic.ttf");
		font-weight: 200;
		font-style: italic;
	}
	@font-face {
		font-family: "gotham";
		src: url("/fonts/gotham/Gotham-Light.ttf");
		font-weight: 400;
		font-style: normal;
	}
	@font-face {
		font-family: "gotham";
		src: url("/fonts/gotham/Gotham-LightItalic.ttf");
		font-weight: 400;
		font-style: italic;
	}
	@font-face {
		font-family: "gotham";
		src: url("/fonts/gotham/Gotham-Book.ttf");
		font-weight: 600;
		font-style: normal;
	}
	@font-face {
		font-family: "gotham";
		src: url("/fonts/gotham/Gotham-Bold.ttf");
		font-weight: 800;
		font-style: normal;
	}
	@font-face {
		font-family: "gotham";
		src: url("/fonts/gotham/Gotham-BoldItalic.ttf");
		font-weight: 800;
		font-style: italic;
	}
	@font-face {
		font-family: "gotham";
		src: url("/fonts/gotham/Gotham-Black.ttf");
		font-weight: 1000;
		font-style: normal;
	}
	@font-face {
		font-family: "gotham";
		src: url("/fonts/gotham/Gotham-BlackItalic.ttf");
		font-weight: 1000;
		font-style: italic;
	}


	@font-face {
		font-family: "trento";
		src: url("/fonts/trento/trento.ttf");
		font-weight: 600;
		font-style: normal;
	}


	@font-face {
		font-family: "august";
		src: url("/fonts/august/august.ttf");
		font-weight: 600;
		font-style: normal;
	}

	:root {
		--color-verde: #132F19;
		--color-almendra: #BAA57D;
		--color-lino: #E8E1DC;
		--color-hueso: #F7F7F5;
		--color-background: #F1F1EF;
	}

	.color-almendra {
		color: var(--color-almendra);
	}

	.color-blanco {
		color: white;
	}

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

	h1, h2, h3, h4, ul {
		margin: 0;
	}

	.content {
		max-width: 1280px;
		margin: 0 auto;
		padding: 0 140px;
		box-sizing: border-box;
	}

	.smaller-text {
		font-size: 13px;
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

	.flex {
		display: flex;
	}

	.col-20 {
		width: 20%;
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
	}

	.padding-top-bottom-30 {
		padding: 30px;
	}

	.padding-top-30 {
		padding-top: 30px;
	}

	.padding-top-50 {
		padding-top: 50px;
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

	.padding-top-200 {
		padding-top: 200px;
	}

	.padding-left-60 {
		padding-left: 60px;
	}

	.padding-top-180 {
		padding-top: 180px;
	}

	h3 {
		font-size: 50px;
		color: var(--color-almendra);
		font-family: mirage;
		font-weight: 200;
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

	p.border-bottom {
		border-bottom: 1px solid;
	}
	
	.uppercase {
		text-transform: uppercase;
	}

	.text-align-right {
		text-align: right;
	}

	.green-background {
		background-color: var(--color-verde);
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

	.text-right {
		text-align: right;
	}

	.block-center {
		margin: 0 auto;
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

	.slide h4 {
		position: absolute;
		top: 38%;
		color: white;
		text-align: center;
		width: 100%;
		font-size: 15px;
		font-family: gotham;
	}
	.slide strong {
		position: absolute;
		top: 48%;
		text-align: center;
		width: 100%;
		display: block;
		color: white;
		font-family: trento;
		font-size: 10px;
	}

	li {
		color: var(--color-almendra);
		font-family: gotham;
		font-size: 14px;
		margin: 12px 0 0;
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

	.signature.color-blanco {
		color: white;
		font-size: 36px;
		position: relative;
		top: -16px;
	}

	.logo-r {
		width: 60px;
	}

	.link-map {
		display: inline-block;
		margin-right: 20px;
		position: relative;
		top: -7px;
		border-bottom: 1px solid;
	}

	.social-media {
		display: inline-flex;
	}

	.social-media img {
		width: 25px;
		margin-right: 6px;
	}

	@media (max-width: 480px) {
		.content {
			padding: 12px;
		}
		.padding-left-60 {
			padding-left: 0;
		}
		h1 {
			padding-left: 20px;
			font-size: 40px;
		}
		.title span {
			margin-left: 20px;
		}
		.chevron-wrapper {
			width: 100%;
		}
		.flex {
			display: block;
		}
		.brand {
			font-size: 10px;
		}
		.signature.color-blanco {
			font-size: 50px;
			top: -20px;
		}
		.col-33 {
			width: auto;
		}
		.col-30 {
			width: auto;
		}
		.row {
			display: block;
		}
		.col-50 {
			width: auto;
		}
		.carousel {
			padding-top: 100px;
		}
		h3 span {
			text-align: initial;
		}
		ul {
			margin-bottom: 200px;
		}
	}
</style>

<svelte:head>
	<title>Sapper project template</title>
</svelte:head>


<div class="cover">
	<div class="banner"></div>
	<div class="top">
		<div class="content col-100">
			<div class="header">
				<h2>HOTEL MÉXICO EN LA PIEL <span>®</span></h2>
				<div>RESERVA</div>
			</div>

			<div class="title">
				<h1>Un homenaje <span>a nuestro México</span></h1>
			</div>
		</div>
	</div>
</div>


<Nav />

<div class="backgroun-light">
	<div class="content">
		<div class="row padding-top-150">
			<div class="col-382">
				<h3>Regresa <span>a casa</span></h3>
				<p class="padding-top-30">
					La calidez de nuestra tierra convertida en un espacio que te abraza, te da la bienvenida y parece que nunca se acaba.
				</p>
				<div class="padding-top-80">
					<Button href="/habitaciones" className="small-arrow">ver habitaciones</Button>
				</div>
			</div>
			<div class="carousel">
				<div class="slide">
					<img src="/homepage/carousel_a/image_a.jpg" alt="">
					<h4>CASA</h4>
					<strong>CHIHUAHUA</strong>
				</div>

				<div class="arrows">
					<div class="col-20">
						<Arrow className="left-arrow" />
					</div>
					<div class="col-20">
						<Arrow className="right-arrow" />
					</div>
				</div>
			</div>
		</div>
	</div>
</div>


<div class="backgroun-light">
	<div class="content">
		<div class="row padding-top-200">
			<div>
				<img src="/homepage/copas_y_vino.jpg" alt="">
			</div>
			<div class="col-50">
				<h3>El Hotel de México, <span class="text-align-right">y el vino</span></h3>
				<p class="padding-top-50">Arquitectura que emerge de la tierra y se fusionan con su entorno, 13 “casas” que rinden homenaje a nuestro México, habitaciones con jacuzzi privado y una ubicación inigualable entre viñedos, áreas rocosas y un sorprendente bosque de encinos, distintas atmósferas dispuestas para emular de manera natural el territorio mexicano; una extensión de 15 hectáreas en donde espacios íntimos y de descanso convergen con espacios de celebración.</p>
				<br />
				<p class="col-75">Te invitamos a celebrar nuestra cultura y disfrutar de nuestra tierra.</p>
				<div class="padding-top-100">
					<Button href="/reserva" className="large-arrow">reserva ahora</Button>
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

	<div class="row padding-top-100">
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
		<div class="green-background">
			<div class="flex padding-top-bottom-30">
				<img src="/homepage/carousel_b/image_a.jpg" alt="">
				<div class="padding-left-60 col-100">
					<h3 class="padding-top-50">Naturaleza</h3>

					<img class="padding-top-50 icon-b" src="/support/icon-b.svg" alt="">

					<div class="padding-top-180">
						<div class="arrows">
							<div class="col-25">
								<Arrow className="left-arrow white-arrow" />
							</div>
							<div class="col-25">
								<Arrow className="right-arrow white-arrow" />
							</div>
						</div>
					</div>
				</div>
			</div>
		</div>
	</div>
</div>


<div class="backgroun-light">
	<div class="content padding-top-100 text-center">
		<p class="text-center strong">HOTEL</p>

		<div class="brand padding-top-30">México</div>
		<div class="signature">en la Piel</div>

		<p class="text-center strong">VALLE DE GUADALUPE</p>

		<br />

		<p class="padding-top-100 col-58 block-center">
			Excelencia en cada detalle para que puedas disfrutar del Valle de Guadalupe en todas sus expresiones, desde su clima mediterráneo y sus paisajes espectaculares hasta el sabor de su comida y sus vinos más selectos.
		</p>
		<br />
		<p class="text-center col-40 block-center">
			Una experiencia exclusiva y reconfortante, para celebrar el amor por México y el Valle de Guadalupe.
		</p>
	</div>
	<div class="padding-top-100"></div>
</div>


<div class="green-background">
	<div class="content">
		<div class="row padding-top-100">
			<div>
				<p class="color-almendra">El hotel de</p>
				<div class="signature color-blanco">México y el Vino</div>
				<p class="uppercase color-almendra border-bottom padding-top-50">HOTEL MÉXICO EN LA PIEL &#169;2021</p>
			</div>
			<div class="padding-top-30">
				<img src="/support/logo-r.svg" alt="" class="logo-r">
			</div>
			<div>
				<p class="color-almendra text-right">
					hola@hotelmexicoenlapiel.com
				</p>
				<p class="color-almendra uppercase smaller-text text-right">
					VALLE DE GUADALUPE, BC, MX.
				</p>
				<p class="color-almendra padding-top-80">
					<a class="link-map" href="https://www.google.com/maps">Google Maps</a>
					<span class="social-media">
						<img src="/support/yelp.svg" alt="">
						<img src="/support/tripadvisor.svg" alt="">
						<img src="/support/facebook.svg" alt="">
						<img src="/support/instagram.svg" alt="">
					</span>
				</p>
			</div>
		</div>
	</div>
	<div class="padding-top-100"></div>
</div>

