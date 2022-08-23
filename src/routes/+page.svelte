<script lang="ts">
	import Counter from '$lib/Counter.svelte';
	import Fa from 'svelte-fa';
	import { faSearch, faEllipsisVertical } from '@fortawesome/free-solid-svg-icons';

</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<main class="w-full">
	<header class="w-full p-2 flex flex-row">
		<article class="w-full my-3 flex flex-row justify-between items-center">
			<span class="">
				<span class="p-2 w-4 h-4 rounded-full bg-current">N/A</span>
				<span class="font-bold text-2xl">Let's Roll</span>
			</span>

			<span class="flex text-gray-500">
				<span class="mx-2"><Fa icon={faSearch} /></span>
				<span class="mx-2"><Fa icon={faEllipsisVertical} /></span>
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
