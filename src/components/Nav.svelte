<script>
	import { onMount } from 'svelte';

	export let segment;
	let isFixed = false;
	let isOpen = false

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

	function toggleMenu() {
		isOpen = !isOpen
	}
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
		right: -14px;
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

	.mobile-menu {
		display: none;
	}

	@media (max-width: 540px) {
		nav {
			position: absolute;
			left: 0;
			top: 74px;
			z-index: 2;
			width: 100%;
			background-color: var(--color-verde);
		}
		li, li a {
			width: 100%;
		}
		a {
			padding: 20px;
			box-sizing: border-box;
		}
		.content {
			padding: 0 12px;
			position: relative;
		}

		.mobile-menu {
			display: block;
			position: relative;
			text-align: right;
		}

		.mobile-menu:after {
			content: '\2807';
			font-size: 50px;
			color: var(--color-lino);
		}
		[aria-current]::after {
			left: 8px;
		}
		.visible {
			display: block;
		}
		.hide {
			display: none;
		}
	}
</style>

<header class={isFixed ? 'fixed' : ''}>
	<div class="content">
		<div class="logo">
			<img src="/support/logo-mini.svg" alt="">
		</div>
		<div class="mobile-menu" on:click={toggleMenu}></div>
		<nav class={isOpen ? 'visible' : 'hide'}>
			<ul>
				<li><a aria-current="{segment === undefined ? 'page' : undefined}" href=".">inicio</a></li>
				<li><a aria-current="{segment === 'habitaciones' ? 'page' : undefined}" href="habitaciones">habitaciones</a></li>
				<!-- <li><a aria-current="{segment === 'cava-cocina' ? 'page' : undefined}" href="cava-cocina">cava y cocina</a></li>
				<li><a aria-current="{segment === 'amenidades' ? 'page' : undefined}" href="amenidades">amenidades</a></li> -->
				<li><a aria-current="{segment === 'contacto' ? 'page' : undefined}" href="contacto">contacto</a></li>
				<li><a href="https://www.airbnb.com/users/200220394/listings" target="_blank">reserva</a></li>
			</ul>
		</nav>
	</div>
</header>
