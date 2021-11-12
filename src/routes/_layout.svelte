<script>
	import Nav from '../components/Nav.svelte';
	import Footer from '../components/Footer.svelte'

	export let segment;
</script>

<style>
	:global(html,body,#sapper,main) {
		height: 100%;
	}
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
	main {
		box-sizing: border-box;
	}
</style>

<link rel="icon" type="image/svg+xml" href="/support/logo-mini.svg">

{#if segment !== undefined && segment !== 'amenidades'}
	<Nav {segment}/>
{/if}
<main>
	<slot></slot>
	<Footer />
</main>
