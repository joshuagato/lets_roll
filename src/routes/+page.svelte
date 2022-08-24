<script lang="ts">
	import Counter from '$lib/Counter.svelte';
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
				<span class="mx-3">
					<svg style="width:24px;height:24px" viewBox="0 0 24 24">
						<path fill="currentColor" d="M9.5,3A6.5,6.5 0 0,1 16,9.5C16,11.11 15.41,12.59 14.44,13.73L14.71,14H15.5L20.5,19L19,20.5L14,15.5V14.71L13.73,14.44C12.59,15.41 11.11,16 9.5,16A6.5,6.5 0 0,1 3,9.5A6.5,6.5 0 0,1 9.5,3M9.5,5C7,5 5,7 5,9.5C5,12 7,14 9.5,14C12,14 14,12 14,9.5C14,7 12,5 9.5,5Z" />
					</svg>
				</span>
				<span class="mx-3">
					<svg style="width:24px;height:24px" viewBox="0 0 24 24">
						<path fill="currentColor" d="M12,16A2,2 0 0,1 14,18A2,2 0 0,1 12,20A2,2 0 0,1 10,18A2,2 0 0,1 12,16M12,10A2,2 0 0,1 14,12A2,2 0 0,1 12,14A2,2 0 0,1 10,12A2,2 0 0,1 12,10M12,4A2,2 0 0,1 14,6A2,2 0 0,1 12,8A2,2 0 0,1 10,6A2,2 0 0,1 12,4Z" />
					</svg>
				</span>
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
							<svg xmlns="http://www.w3.org/2000/svg" height="24" viewBox="0 0 24 24" width="24">
								<path d="M0 0h24v24H0z" fill="none"/>
								<path d="M10 6L8.59 7.41 13.17 12l-4.58 4.59L10 18l6-6z"/>
							</svg>
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
