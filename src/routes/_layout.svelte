<script>
	import Nav from '../components/Nav.svelte';

	export let segment;
</script>

<style>
	:global(html,body,#sapper,main) {
		height: 100%;
	}
	main {
		box-sizing: border-box;
	}
</style>

{#if segment !== undefined}
	<Nav {segment}/>
{/if}
<main>
	<slot></slot>
</main>
