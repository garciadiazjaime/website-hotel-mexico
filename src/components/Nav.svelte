<script>
	export let segment;
</script>

<style>
	header {
		background-color: darkolivegreen;
		color: white;
	}

 	nav {
		font-weight: 300;
		display: flex;
		justify-content: space-between;
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
	}

	a:last-of-type {
		padding-right: 0;
	}

	.content {
		max-width: 1328px;
		margin: 0 auto;
		display: flex;
		justify-content: space-between;
	}

	.logo {
		margin: auto 0;
	}

	img {
		display: block;
	}
</style>

<header>
	<div class="content">
		<div class="logo">
			<img src="https://via.placeholder.com/25x40" alt="">
		</div>
		<nav>
			<ul>
				<li><a aria-current="{segment === undefined ? 'page' : undefined}" href=".">inicio</a></li>
				<li><a aria-current="{segment === 'habitaciones' ? 'page' : undefined}" href="habitaciones">habitaciones</a></li>
				<li><a aria-current="{segment === 'cava-cocina' ? 'page' : undefined}" href="cava-cocina">cava y cocina</a></li>
				<li><a aria-current="{segment === 'amenidades' ? 'page' : undefined}" href="amenidades">amenidades</a></li>
				<li><a aria-current="{segment === 'reserva' ? 'page' : undefined}" href="reserva">reserva</a></li>
			</ul>
		</nav>
	</div>
</header>
