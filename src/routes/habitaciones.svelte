<script>
	import Subheader from '../components/Subheader.svelte';
	import CabinCard from '../components/CabinCard.svelte';

	const cabins = [
		{
			name: 'Casa Sonora',
			images: [
				{
				 path: 'https://picsum.photos/1000/400?random=1',
				 id: 'img1',
				},
				{
				 path: 'https://picsum.photos/1000/400?random=2',
				 id: 'img2',
				},
				{
				 path: 'https://picsum.photos/1000/400?random=3',
				 id: 'img3',
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
		}
	];
</script>

<Subheader color="red">Habitaciones</Subheader>
<h1>Amar al Valle es amar a México</h1>
<hr>
<p>Cómodas habitaciones te darán la bienvenida, amenidades de lujo y un staff de primer nivel harán de tu estancia una experiencia inolvidable.</p>
{#each cabins as cabin}
	<CabinCard cabinData={cabin} />
{/each}
<a href='/'>Ver más</a>
