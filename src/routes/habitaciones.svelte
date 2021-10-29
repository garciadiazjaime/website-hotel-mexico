<script>
	import Subheader from '../components/Subheader.svelte';
	import CabinCard from '../components/CabinCard.svelte';

	import { onMount } from 'svelte';

  let Carousel;
  onMount(async () => {
    const module = await import('svelte-carousel');
    Carousel = module.default;
  });

	const cabins = [
		{
			name: 'Sonora',
			images: [
				{
				 path: 'https://picsum.photos/1000/400?random=1',
				 id: 'son1',
				},
				{
				 path: 'https://picsum.photos/1000/400?random=2',
				 id: 'son2',
				},
				{
				 path: 'https://picsum.photos/1000/400?random=3',
				 id: 'son3',
				},
			],
			caracteristicas: [
				'Cama queen size',
				'Baño y regadera',
				'Sala con chimenea',
				'Barra comedor',
				'Patio terraza',
			],
			amenidades: [
				'Limpieza',
				'Refrigerador',
				'Televisión',
				'Internet (wi-fi)',
				'Aire (AC)',
			],
			reservationUrl: 'http://reservationurl.com',
		},
		{
			name: 'Sinaloa',
			images: [
				{
				 path: 'https://picsum.photos/1000/400?random=4',
				 id: 'sin1',
				},
				{
				 path: 'https://picsum.photos/1000/400?random=5',
				 id: 'sin2',
				},
				{
				 path: 'https://picsum.photos/1000/400?random=6',
				 id: 'sin3',
				},
			],
			caracteristicas: [
				'Cama queen size',
				'Baño y regadera',
				'Sala con chimenea',
				'Barra comedor',
				'Patio terraza',
			],
			amenidades: [
				'Limpieza',
				'Refrigerador',
				'Televisión',
				'Internet (wi-fi)',
				'Aire (AC)',
			],
			reservationUrl: 'http://reservationurl.com',
		},
		{
			name: 'Chihuahua',
			images: [
				{
				 path: 'https://picsum.photos/1000/400?random=7',
				 id: 'chi1',
				},
				{
				 path: 'https://picsum.photos/1000/400?random=8',
				 id: 'chi2',
				},
				{
				 path: 'https://picsum.photos/1000/400?random=39',
				 id: 'chi3',
				},
			],
			caracteristicas: [
				'Cama queen size',
				'Baño y regadera',
				'Sala con chimenea',
				'Barra comedor',
				'Patio terraza',
			],
			amenidades: [
				'Limpieza',
				'Refrigerador',
				'Televisión',
				'Internet (wi-fi)',
				'Aire (AC)',
			],
			reservationUrl: 'http://reservationurl.com',
		},
		{
			name: 'Durango',
			images: [
				{
				 path: 'https://picsum.photos/1000/400?random=19',
				 id: 'dur1',
				},
				{
				 path: 'https://picsum.photos/1000/400?random=28',
				 id: 'dur2',
				},
				{
				 path: 'https://picsum.photos/1000/400?random=37',
				 id: 'dur3',
				},
			],
			caracteristicas: [
				'Cama queen size',
				'Baño y regadera',
				'Sala con chimenea',
				'Barra comedor',
				'Jacuzzi exterior',
				'Patio terraza',
			],
			amenidades: [
				'Limpieza',
				'Refrigerador',
				'Televisión',
				'Internet (wi-fi)',
				'Aire (AC)',
			],
			reservationUrl: 'http://reservationurl.com',
		},
		{
			name: 'Coahuila',
			images: [
				{
				 path: 'https://picsum.photos/1000/400?random=16',
				 id: 'coa1',
				},
				{
				 path: 'https://picsum.photos/1000/400?random=25',
				 id: 'coa2',
				},
				{
				 path: 'https://picsum.photos/1000/400?random=34',
				 id: 'coa3',
				},
			],
			caracteristicas: [
				'Cama queen size',
				'Baño y regadera',
				'Sala con chimenea',
				'Barra comedor',
				'Jacuzzi exterior',
				'Patio terraza',
			],
			amenidades: [
				'Limpieza',
				'Refrigerador',
				'Televisión',
				'Internet (wi-fi)',
				'Aire (AC)',
			],
			reservationUrl: 'http://reservationurl.com',
		}
	];
</script>

<style>
	.main {
		background: white;
		padding:30px 20px 60px;
	}
	.catalog {
		background: lightgray;
		margin: 0 auto;
		position: relative;
	}

	.catalog:before {
		content: '';
		display: block;
		width: 100%;
		height: 40px;
		background-color: white;
		position: absolute;
		top: 0;
		left: 0;
		z-index: 0;
	}
	hr {
		border: none;
		margin: 0 auto 60px;
		position: relative;
		width: 1px;
		height: 1px;
		overflow: visible;

	}
	hr:before {
		content: '';
		display: block;
		position: absolute;
		left: 0;
		top: 0;
		width: 30px;
		height: 30px;
		border-color: goldenrod;
		border-top: solid 1px goldenrod;
		border-right: solid 1px goldenrod;
		transform: rotate(-45deg);
	}
	hr:after {
		content: '';
		position: absolute;
		display: block;
		left: 0;
		top: -20px;
		width: 30px;
		height: 30px;
		background: none;
		margin: 0 auto;
		border-color: goldenrod;
		border-bottom: solid 1px goldenrod;
		border-left: solid 1px goldenrod;
		transform: rotate(-45deg);
	}
	h1 {
		color: goldenrod;
		text-align: center;
		margin: 60px 0 40px;
	}
	p {
		max-width: 50%;
		text-align: center;
		margin: 0 auto 80px;
		color: black;
	}
	.ver-mas {
		display: block;
		margin: 0 auto;
		text-align: center;
		color: goldenrod;
		text-transform: uppercase;
		position: relative;
		margin-bottom: 30px;
		padding-bottom: 40px;
		text-decoration: none;
	}
	.ver-mas:before, .ver-mas:after {
		content: '';
		border-right: 1px solid goldenrod;
		border-bottom: 1px solid goldenrod;
		transform: rotate(45deg) translateX(-50%);
		position: absolute;
		left: 50%;
		border-radius: 3px;
	}
	.ver-mas:before {
		width: 30px;
		height: 30px;
		bottom: 0;
	}
	.ver-mas:after {
		width: 24px;
		height: 24px;
		bottom: 8px;
	}
</style>

<div class='main'>
	<Subheader color="goldenrod">Habitaciones</Subheader>
	<h1>Amar al Valle es amar a México</h1>
	<hr>
	<p>Cómodas habitaciones te darán la bienvenida, amenidades de lujo y un staff de primer nivel harán de tu estancia una experiencia inolvidable.</p>
</div>
<div class="catalog">
	{#each cabins as cabin}
		<CabinCard cabinData={cabin} Carousel={Carousel} />
	{/each}
	<a class='ver-mas' href='/'>Ver más</a>
</div>
