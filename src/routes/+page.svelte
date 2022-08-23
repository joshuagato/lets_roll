<script lang="ts">
	import Counter from '$lib/Counter.svelte';
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<main>
	<header>
		<p>header</p>
	</header>

	<section>
		<p>filters</p>
	</section>
	<section>
		<p>profiles</p>
	</section>

	<footer>
		<p>footer</p>
	</footer>
</main>

<style lang="scss">
	main {
		display: grid;
		grid-template-areas:
		"header"
		"filters"
		"profiles"
		"footer";
	}

	h1 {
		width: 100%;
	}

	.welcome {
		display: block;
		position: relative;
		width: 100%;
		height: 0;
		padding: 0 0 calc(100% * 495 / 2048) 0;
	}

	.welcome img {
		position: absolute;
		width: 100%;
		height: 100%;
		top: 0;
		display: block;
	}
</style>
