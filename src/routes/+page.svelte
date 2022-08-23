<script lang="ts">
	import Counter from '$lib/Counter.svelte';
	import Fa from 'svelte-fa';
	import { faSearch, faEllipsisVertical } from '@fortawesome/free-solid-svg-icons';

</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<main class="">
	<header class="flex flex-row">
		<article class="w-full my-3 flex flex-row justify-between items-center">
			<span class="flex items-center">
				<span class="block p-2 h-11 w-11 rounded-full bg-pink-600
				text-gray-50 text-center mx-auto font-bold mx-1">N/A</span>
				<span class="font-bold text-2xl mx-1">Let's Roll</span>
			</span>

			<span class="flex text-gray-500">
				<span class="mx-3"><Fa size="xl" icon={faSearch} /></span>
				<span class="mx-3"><Fa icon={faEllipsisVertical} /></span>
			</span>
		</article>
	</header>

	<section class="w-full">
		<p>filters</p>
	</section>
	<section class="w-full">
		<p>profiles</p>
	</section>

	<footer class="w-full">
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

	//.welcome {
	//	display: block;
	//	position: relative;
	//	width: 100%;
	//	height: 0;
	//	padding: 0 0 calc(100% * 495 / 2048) 0;
	//}
	//
	//.welcome img {
	//	position: absolute;
	//	width: 100%;
	//	height: 100%;
	//	top: 0;
	//	display: block;
	//}
</style>
