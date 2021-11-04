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

	:root {
		--color-verde: #132F19;
		--color-almendra: #BAA57D;
		--color-lino: #E8E1DC;
		--color-hueso: #F7F7F5;
		--color-background: #F1F1EF;
	}

	.color-verde {
		color: var(--color-verde)
	}

	.font-gotham {
		font-family: gotham;
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

	.content {
		max-width: 1280px;
		margin: 0 auto;
		padding: 0 50px;
	}
	
	.cover {
		position: relative;
		height: 90%;
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

	@media (max-width: 480px) {
		h1 {
			padding-left: 20px;
			font-size: 40px;
		}
		.title span {
			margin-left: 20px;
		}
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

	.placeholder_f {
		width: 400px;
		height: 100px;
		border: 1px solid black;
	}

	.placeholder_g {
		width: 50px;
		height: 150px;
		border: 1px solid black;
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

	.col-30 {
		width: 30%;
	}

	.col-33 {
		width: calc(100%/3);
	}

	.col-50 {
		width: 50%;
	}

	.col-60 {
		width: 60%;
	}

	.col-75 {
		width: 75%;
	}

	.col-100 {
		width: 100%;
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
		padding-top: 40px;
		font-size: 50px;
		color: var(--color-almendra);
		font-family: mirage;
		font-weight: 200;
	}

	h3 span {
		display: block;
		text-align: right;
	}

	p {
		color: var(--color-verde);
		font-family: gotham;
		text-align: justify;
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

	.chevron-arrow-up::before {
		content: '';
		display: inline-block;
		border-right: 1px solid var(--color-almendra);
		border-bottom: 1px solid var(--color-almendra);
		width: 16px;
		height: 16px;
		transform: rotate(225deg);
	}

	.chevron-arrow-up::after {
		content: '';
		display: inline-block;
		border-right: 1px solid var(--color-almendra);
		border-bottom: 1px solid var(--color-almendra);
		width: 16px;
		height: 16px;
		transform: rotate(225deg);
		position: absolute;
		top: 6px;
		left: 0;
	}

	.chevron-arrow-down::before {
		content: '';
		display: inline-block;
		border-right: 1px solid var(--color-almendra);
		border-bottom: 1px solid var(--color-almendra);
		width: 16px;
		height: 16px;
		transform: rotate(45deg);
		position: relative;
		top: -10px;
		left: 0;
	}

	.chevron-arrow-down::after {
		content: '';
		display: inline-block;
		border-right: 1px solid var(--color-almendra);
		border-bottom: 1px solid var(--color-almendra);
		width: 16px;
		height: 16px;
		transform: rotate(45deg);
		position: absolute;
		top: -4px;
		left: 0;
	}

	.display-flex {
		display: flex;
	}

	.margin-right {
		margin-right: 15px;
	}

	.justify-contet-center {
		justify-content: center;
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

	.slide {
		position: relative;
	}

	.chevron-wrapper {
		position: relative;
		top: 16px;
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
		font-size: 23px;
		margin: 12px 0;
	}

	.icon-b {
		width: 44px;
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
			<div class="col-30">
				<h3 class="col-50">Regresa <span>a casa</span></h3>
				<p class="padding-top-30">
					La calidez de nuestra tierra convertida en un espacio que te abraza, te da la bienvenida y parece que nunca se acaba.
				</p>
				<div class="padding-top-80">
					<Button href="/habitaciones" className="small-arrow">ver habitaciones</Button>
				</div>
			</div>
			<div>
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
				<h3 class="padding-top-80 col-75">El Hotel de México, <span>y el vino</span></h3>
				<p class="padding-top-50">Arquitectura que emerge de la tierra y se fusionan con su entorno, 13 “casas” que rinden homenaje a nuestro México, habitaciones con jacuzzi privado y una ubicación inigualable entre viñedos, áreas rocosas y un sorprendente bosque de encinos, distintas atmósferas dispuestas para emular de manera natural el territorio mexicano; una extensión de 15 hectáreas en donde espacios íntimos y de descanso convergen con espacios de celebración.</p>
				<p class="col-50">Te invitamos a celebrar nuestra cultura y disfrutar de nuestra tierra.</p>
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
			<p class="col-75">Una experiencia exclusiva que le permitirá a cada uno de nuestros huéspedes explorar con todos sus sentidos los sabores de México, la riqueza de su tierra y sentir a flor de piel nuestra pasión por la cultura mexicana.</p>
			<ul class="padding-top-50">
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
	<div class="padding-top-200 display-flex justify-contet-center chevron-wrapper">
		<div class="chevron-arrow-up position-relative margin-right"></div>
		<div class="chevron-arrow-down position-relative margin-right"></div>
		<div class="chevron-arrow-up position-relative margin-right"></div>
		<div class="chevron-arrow-down position-relative margin-right"></div>
		<div class="chevron-arrow-up position-relative margin-right"></div>
		<div class="chevron-arrow-down position-relative margin-right"></div>
		<div class="chevron-arrow-up position-relative margin-right"></div>
		<div class="chevron-arrow-down position-relative margin-right"></div>
		<div class="chevron-arrow-up position-relative margin-right"></div>
		<div class="chevron-arrow-down position-relative margin-right"></div>
		<div class="chevron-arrow-up position-relative margin-right"></div>
		<div class="chevron-arrow-down position-relative margin-right"></div>
		<div class="chevron-arrow-up position-relative margin-right"></div>
		<div class="chevron-arrow-down position-relative margin-right"></div>
		<div class="chevron-arrow-up position-relative margin-right"></div>
		<div class="chevron-arrow-down position-relative margin-right"></div>
		<div class="chevron-arrow-up position-relative margin-right"></div>
		<div class="chevron-arrow-down position-relative margin-right"></div>
		<div class="chevron-arrow-up position-relative margin-right"></div>
		<div class="chevron-arrow-down position-relative margin-right"></div>
		<div class="chevron-arrow-up position-relative margin-right"></div>
		<div class="chevron-arrow-down position-relative margin-right"></div>
		<div class="chevron-arrow-up position-relative margin-right"></div>
		<div class="chevron-arrow-down position-relative margin-right"></div>
	</div>
</div>


<div class="backgroun-light padding-top-200">
	<div class="content">
		<div class="green-background">
			<div class="flex padding-top-bottom-30">
				<img src="/homepage/carousel_b/image_a.jpg" alt="">
				<div class="padding-left-60 col-100">
					<h3 class="padding-top-100">Naturaleza</h3>

					<img class="padding-top-100 icon-b" src="/support/icon-b.svg" alt="">

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
