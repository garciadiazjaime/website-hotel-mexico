<script>
	export let segment;
</script>

<style>
	nav {
		border-bottom: 1px solid rgba(255,62,0,0.1);
		font-weight: 300;
		padding: 0 1em;
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
		background-color: rgb(255,62,0);
		display: block;
		bottom: -1px;
	}

	a {
		text-decoration: none;
		padding: 1em 0.5em;
		display: block;
		text-transform: uppercase;
	}

	.content {
		max-width: 1328px;
		margin: 0 auto;
	}
</style>

<header>
	<div class="content">
		<div class="logo">
			logo
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
