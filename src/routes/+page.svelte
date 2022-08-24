<script lang="ts">
	import Counter from '$lib/Counter.svelte';
	import Fa from 'svelte-fa';
	import { faSearch, faEllipsisVertical, faChevronRight } from '@fortawesome/free-solid-svg-icons';
	const data = [
		{ id: 1, name: 'Irma Flores', date: '16/12/2019', picture: 'profile_1.jpg', description: 'This is the first phrase or clause of my chat.' },
		{ id: 2, name: 'Irma Flores', date: '16/12/2019', picture: 'profile_2.jpeg', description: 'This is the first phrase or clause of my chat.' },
		{ id: 3, name: 'Irma Flores', date: '16/12/2019', picture: 'profile_3.jpg', description: 'This is the first phrase or clause of my chat.' },
		{ id: 1, name: 'Irma Flores', date: '16/12/2019', picture: 'profile_1.jpg', description: 'This is the first phrase or clause of my chat.' },
		{ id: 2, name: 'Irma Flores', date: '16/12/2019', picture: 'profile_2.jpeg', description: 'This is the first phrase or clause of my chat.' },
		{ id: 3, name: 'Irma Flores', date: '16/12/2019', picture: 'profile_3.jpg', description: 'This is the first phrase or clause of my chat.' }
	];
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<main>
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
		<ul class="flex justify-between items-center text-xs font-bold">
			<li class="text-orange-500">FRIENDS</li>
			<li class="text-blue-400">TO SELLERS</li>
			<li class="text-blue-400">MY CUSTOMERS</li>
			<li class="text-blue-400">DELIVERY</li>
		</ul>
	</section>
	<section class="w-full my-4">
		{#if data && data.length > 0}
			{#each data as {id, name, date, picture, description}}
				<article class="flex items-center content-between pl-0 ml-0 my-3">
					<aside class="w-1/5 ">
						<img class="rounded-full h-16 w-16" src="{picture}" alt="">
					</aside>
					<div class="w-4/5 flex flex-col pl-2">
						<div class="flex justify-between items-center">
					<span class="font-bold">
						{name}
					</span>
							<div class="flex items-center">
						<span class="text-gray-400 mx-2">
							{date}
						</span>
								<span class="text-gray-400 mx-2">
							<Fa icon={faChevronRight} />
						</span>
							</div>
						</div>
						<div class="text-gray-400 text-sm">
							{description}
						</div>
					</div>
				</article>
				<hr class="border-gray-400 border-t-1 my-2" />
			{/each}
		{/if}
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
	//}/
	//
	//.welcome img {
	//	position: absolute;
	//	width: 100%;
	//	height: 100%;
	//	top: 0;
	//	display: block;
	//}
</style>
