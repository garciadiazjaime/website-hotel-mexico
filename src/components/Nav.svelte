<script>
	import { onMount } from 'svelte';

	export let segment;
	let isFixed = false;

	onMount(() => {
		const element = document.querySelector('.banner');
		if (!element) {
			return
		}
		const handleIntersection = (entries) => {
			for (let entry of entries) {
				isFixed = !entry.isIntersecting
			}
		}

		const observer = new IntersectionObserver(handleIntersection);
		observer.observe(element);
	})

</script>

<style>
	:root {
		--color-verde: #132F19;
		--color-almendra: #BAA57D;
		--color-lino: #E8E1DC;
		--color-hueso: #F7F7F5;
		--color-background: #F1F1EF;
	}

	header {
		background-color: var(--color-verde);
		color: white;
		z-index: 1;
		width: 100%;
	}

 	nav {
		font-weight: 300;
		display: flex;
		justify-content: space-between;
		background-color: var(--color-verde);
	}

	ul {
		margin: 0;
		padding: 0;
	}

	/* clearfix */
	ul::after {
		content: '';
		display: block;
		clear: both;
	}

	li {
		display: block;
		float: left;
	}

	[aria-current] {
		position: relative;
		display: inline-block;
	}

	[aria-current]::after {
		position: absolute;
		content: '';
		width: calc(100% - 1em);
		height: 2px;
		background-color: white;
		display: block;
		bottom: -1px;
	}

	a {
		text-decoration: none;
		padding: 20px 40px;
		display: block;
		text-transform: uppercase;
		font-family: gotham;
		font-size: 14px;
		font-weight: 400;
	}

	a:last-of-type {
		padding-right: 0;
	}

	.content {
		max-width: 1280px;
		margin: 0 auto;
		display: flex;
		justify-content: space-between;
		padding: 0 50px;
		box-sizing: border-box;
	}

	.logo {
		margin: auto 0;
	}

	.logo img {
		display: block;
		height: 40px;
	}

	.fixed {
		position: fixed;
		top: 0px;
	}
</style>

<header class={isFixed ? 'fixed' : ''}>
	<div class="content">
		<div class="logo">
			<img src="/support/logo-mini.svg" alt="">
		</div>
		<nav>
			<ul>
				<li><a aria-current="{segment === undefined ? 'page' : undefined}" href=".">inicio</a></li>
				<li><a aria-current="{segment === 'habitaciones' ? 'page' : undefined}" href="habitaciones">habitaciones</a></li>
				<li><a aria-current="{segment === 'cava-cocina' ? 'page' : undefined}" href="cava-cocina">cava y cocina</a></li>
				<li><a aria-current="{segment === 'amenidades' ? 'page' : undefined}" href="amenidades">amenidades</a></li>
				<li><a href="https://www.airbnb.com/users/200220394/listings" target="_blank">reserva</a></li>
			</ul>
		</nav>
	</div>
</header>
