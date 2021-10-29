<script>
	import Nav from '../components/Nav.svelte';
	import Button from '../components/Button.svelte'
	import Arrow from '../components/Arrow.svelte'
</script>

<style>
	h1 {
		padding-left: 100px;
	}

	img {
		max-width: 100%;
		height: auto;
		display: block;
	}

	.content {
		max-width: 1328px;
		margin: 0 auto;
		width: 100%;
	}

	.cover {
		position: relative;
	}

	.top {
		width: 100%;
		position: absolute;
		top: 0;
		left: 0;
		display: flex;
		justify-content: space-between;
		color: white;
		padding-top: 40px;
	}

	.title {
		position: absolute;
		top: 300px;
		width: 100%;
	}

	.title span {
		display: block;
		margin-left: 80px;
	}

	.header {
		display: flex;
		justify-content: space-between;
	}

	.header span {
		font-size: 12px;
		position: relative;
		top: 3px;
	}

	.arrow {
		position: absolute;
		bottom: 20px;
		width: 100%;
	}

	.arrow img {
		position: relative;
		left: 50%;
	}

	.placeholder_b {
		width: 500px;
		height: 700px;
		border: 1px solid black;
	}

	.placeholder_c {
		width: 500px;
		height: 400px;
		border: 1px solid black;
	}

	.placeholder_d {
		width: 800px;
		height: 400px;
		border: 1px solid black;
	}

	.placeholder_e {
		width: 400px;
		height: 200px;
		border: 1px solid black;
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

	.col-3 {
		width: calc(100%/3);
	}

	.padding1 {
		padding-top: 150px;
	}

	h3 {
		padding-top: 20px;
		font-size: 30px;
	}

	h3 span {
		display: block;
		padding-left: 40px;
	}

	.green_background {
		background-color: darkolivegreen;
	}

	.width-50 {
		width: 50%;
	}

	.padding-top-100 {
		padding-top: 100px;
	}

	.arrows {
		display: flex;
		justify-content: space-between;
		padding-top: 40px;
	}

	.col-4 {
		width: calc(100%/4);
	}

	@media (min-width: 480px) {
		h1 {
			font-size: 4em;
		}
	}
</style>

<svelte:head>
	<title>Sapper project template</title>
</svelte:head>


<div class="cover">
	<img src="https://via.placeholder.com/1750x800" alt="">


	<div class="top">
		<div class="content">
			<div class="header">
				<h2>HOTEL MÉXICO EN LA PIEL <span>®</span></h2>
				<div>RESERVA</div>
			</div>
		</div>

		<div class="title">
			<h1 class="content">Un homenaje <span>a nuestro México</span></h1>
		</div>
	</div>

	<div class="arrow">
		<img src="https://via.placeholder.com/30x30" alt="">
	</div>

</div>

<Nav />

<div class="content row padding1">
	<div class="col-3">
		<h3>Regresa <span>a casa</span></h3>
		<p>
			La calidez de nuestra tierra convertida en un espacio que te abraza, te da la bienvenida y parece que nunca se acaba.
		</p>
		<div class="width-50 padding-top-100">
			<Button href="/habitaciones" className="small-arrow">ver habitaciones</Button>
		</div>
	</div>
	<div>
		<img src="https://via.placeholder.com/750x500" alt="">

		<div class="arrows">
			<div class="col-4">
				<Arrow className="left-arrow" />
			</div>
			<div class="col-4">
				<Arrow className="right-arrow" />
			</div>
		</div>
	</div>
</div>

<div class="content row">
	<div>
		<div class="placeholder_b"></div>
	</div>
	<div>
		<h3>El Hotel de México, y el vino</h3>
		<p>Arquitectura que emerge de la tierra y se fusionan con su entorno, 13 “casas” que rinden homenaje a nuestro México, habitaciones con jacuzzi privado y una ubicación inigualable entre viñedos, áreas rocosas y un sorprendente bosque de encinos, distintas atmósferas dispuestas para emular de manera natural el territorio mexicano; una extensión de 15 hectáreas en donde espacios íntimos y de descanso convergen con espacios de celebración.</p>
		<p>Te invitamos a celebrar nuestra cultura y disfrutar de nuestra tierra.</p>
		<a href="/reserva">reserva ahora</a>
	</div>
</div>

<div class="content">
	<h4>Despertar con todo <br />México ante tus ojos.</h4>
	<div class="row">
		<div>
			<p>Una experiencia exclusiva que le permitirá a cada uno de nuestros huéspedes explorar con todos sus sentidos los sabores de México, la riqueza de su tierra y sentir a flor de piel nuestra pasión por la cultura mexicana.</p>
			<ul>
				<li>Espacios privados</li>
				<li>Casas con jacuzzi</li>
				<li>Servicio a cuarto</li>
				<li>Seguridad 24 hr</li>
				<li>Estacionamiento</li>
				<li>Transporte interno</li>
			</ul>
		</div>
		<div>
			<div class="placeholder_c"></div>
		</div>
	</div>
</div>

<div class="content">
	<div> . . . </div>
</div>

<div class="green_background">
	<div class="content">
		<div class="row">
			<div class="placeholder_d"></div>
			<div>
				Naturaleza
			</div>
		</div>
	</div>
</div>

<div class="content">
	<p>HOTEL</p>
	<div class="placeholder_e"></div>
	<p>VALLE DE GUADALUPE</p>

	<br />

	<p>
		Excelencia en cada detalle para que puedas disfrutar del Valle de Guadalupe en todas sus expresiones, desde su clima mediterráneo y sus paisajes espectaculares hasta el sabor de su comida y sus vinos más selectos.
	</p>
	<p>
		Una experiencia exclusiva y reconfortante, para celebrar el amor por México y el Valle de Guadalupe.
	</p>
</div>


<div class="green_background">
	<div class="content">
		<div class="row">
			<div>
				<p>El hotel de</p>
				<div class="placeholder_f"></div>
				<p>HOTEL MÉXICO EN LA PIEL &#169;2021</p>
				HOTEL
			</div>
			<div>
				<div class="placeholder_g"></div>
			</div>
			<div>
				<p>hola@hotelmexicoenlapiel.com</p>
				<p>VALLE DE GUADALUPE, BC, MX.</p>
				<p>
					<a href="https://www.google.com/maps">Google Maps</a>
					<span>Yelp</span>
					<span>Tripadvisor</span>
					<span>Facebook</span>
					<span>Instagram</span>
				</p>
			</div>
		</div>
	</div>
</div>
