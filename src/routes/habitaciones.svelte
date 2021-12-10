<script>
	import { onMount } from 'svelte';

	import Subheader from '../components/Subheader.svelte';
	import CabinCard from '../components/CabinCard.svelte';
	import cabins from '../support/cabins'


  let Carousel;
	let Lazy
  onMount(async () => {
    const module = await import('svelte-carousel');
    Carousel = module.default;

		const moduleLazy = await import('svelte-lazy');
    Lazy = moduleLazy.default;
  });
</script>

<style>
	.main {
		margin-top: 40px;
		font-family: gotham;
		font-size: 18px;
	}
	.content {
		max-width: 1280px;
		margin: 0 auto;
		padding: 0 50px;
		box-sizing: border-box;
	}
	.intro {
		padding: 0 140px;
	}
	.catalog {
		background-color: var(--color-hueso);
		margin: 0 auto;
		position: relative;
		margin-top: 100px;
		padding-top: 100px;
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
		border-color: var(--color-almendra);
		border-top: solid 1px var(--color-almendra);
		border-right: solid 1px var(--color-almendra);
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
		border-color: var(--color-almendra);
		border-bottom: solid 1px var(--color-almendra);
		border-left: solid 1px var(--color-almendra);
		transform: rotate(-45deg);
	}
	h1 {
		color: var(--color-almendra);
		text-align: center;
		margin: 60px 0 40px;
		font-family: mirage;
		font-weight: 200;
		font-size: 50px;
	}
	p {
		max-width: 570px;
		text-align: center;
		margin: 0 auto 80px;
		color: black;
	}

	:global(body) {
		background: var(--color-hueso);
	}

	@media (max-width: 960px) {
    .content {
      padding: 12px;
    }
		.intro {
			padding: 0;
		}
		.catalog {
      padding: 0;
			margin-top: 0;
    }
  }
</style>
<div class="main">
	<div class="content">
		<Subheader color="var(--color-almendra)">Habitaciones</Subheader>
		<div class="intro">
			<h1>Amar al Valle es amar a México</h1>
			<hr>
			<p>Cómodas habitaciones te darán la bienvenida, amenidades de lujo y un staff de primer nivel harán de tu estancia una experiencia inolvidable.</p>
		</div>
	</div>
	<div class="catalog">
		{#each cabins as cabin}
			<CabinCard cabinData={cabin} Carousel={Carousel} Lazy={Lazy} />
		{/each}
	</div>
</div>
