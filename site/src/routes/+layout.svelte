<script lang="ts">
	import Nav from '$lib/components/Nav.svelte';
	import ScrollUp from '$lib/components/ScrollUp.svelte';
	import '$lib/scss/app.scss';
</script>

<svelte:head>
	<link rel="icon" href="/logo.PNG" />
</svelte:head>

<ScrollUp></ScrollUp>
<Nav></Nav>

<main>
	<slot />
</main>

<style>
	main {
		max-width: 40rem;
		margin-inline: auto;
		padding-inline: 1rem;
	}
</style>
