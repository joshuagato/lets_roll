<script lang="ts">
	import Counter from '$lib/Counter.svelte';
	const data = [
		{ id: 1, name: 'Irma Flores', time: '09:08pm', picture: 'profile_1.jpg', its: 2, mtp: 16 },
		{ id: 2, name: 'Irma Flores', time: 'Today', picture: 'profile_2.jpeg', its: 2, mtp: 16 },
		{ id: 3, name: 'Irma Flores', time: 'Yesterday', picture: 'profile_3.jpg', its: 2, mtp: 16 },
		{ id: 1, name: 'Irma Flores', time: '16/Dec/2019', picture: 'profile_1.jpg', its: 2, mtp: 16 },
		{ id: 2, name: 'Irma Flores', time: '16/May/2019', picture: 'profile_2.jpeg', its: 2, mtp: 16 },
		{ id: 3, name: 'Irma Flores', time: '16/12/2019', picture: 'profile_3.jpg', its: 2, mtp: 16 }
	];
</script>

<svelte:head>
	<title>Inquire</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<main>
	<header class="flex flex-row border-r-rounded-[20px]">
		<article class="w-full h-26 my-3 flex flex-row justify-between items-center">
			<span class="flex items-center">
				<span class="block p-2 h-11 w-11 rounded-full bg-pink-600
				text-gray-50 text-center mx-auto font-bold mx-1">N/A</span>
				<span class="font-medium text-xl not-italic leading-[26px] text-black mx-1">Let's Roll</span>
			</span>

			<span class="flex text-gray-500">
				<span class="mx-3">
					<svg style="width:24px;height:24px" viewBox="0 0 24 24">
						<path fill="currentColor" d="M9.5,3A6.5,6.5 0 0,1 16,9.5C16,11.11 15.41,12.59 14.44,13.73L14.71,14H15.5L20.5,19L19,20.5L14,15.5V14.71L13.73,14.44C12.59,15.41 11.11,16 9.5,16A6.5,6.5 0 0,1 3,9.5A6.5,6.5 0 0,1 9.5,3M9.5,5C7,5 5,7 5,9.5C5,12 7,14 9.5,14C12,14 14,12 14,9.5C14,7 12,5 9.5,5Z" />
					</svg>
				</span>
				<div class="relative">
					<svg style="width:24px;height:24px" viewBox="0 0 24 24">
						<path fill="currentColor" d="M20,14H4V8H9.08L7,10.83L8.62,12L11,8.76L12,7.4L13,8.76L15.38,12L17,10.83L14.92,8H20M20,19H4V17H20M9,4A1,1 0 0,1 10,5A1,1 0 0,1 9,6A1,1 0 0,1 8,5A1,1 0 0,1 9,4M15,4A1,1 0 0,1 16,5A1,1 0 0,1 15,6A1,1 0 0,1 14,5A1,1 0 0,1 15,4M20,6H17.82C17.93,5.69 18,5.35 18,5A3,3 0 0,0 15,2C13.95,2 13.04,2.54 12.5,3.35L12,4L11.5,3.34C10.96,2.54 10.05,2 9,2A3,3 0 0,0 6,5C6,5.35 6.07,5.69 6.18,6H4C2.89,6 2,6.89 2,8V19C2,20.11 2.89,21 4,21H20C21.11,21 22,20.11 22,19V8C22,6.89 21.11,6 20,6Z" />
					</svg>
					<div class="block absolute w-[16px] h-[16px] font-bold flex items-center content-center top-[-8px] right-[-8px] bg-[#FF6600] text-white not-italic leading-[9px] text-[8px] rounded-xl mx-auto text-center"><span class="mx-auto">{30}</span></div>
				</div>
				<span class="mx-3">
					<svg style="width:24px;height:24px" viewBox="0 0 24 24">
						<path fill="currentColor" d="M12,16A2,2 0 0,1 14,18A2,2 0 0,1 12,20A2,2 0 0,1 10,18A2,2 0 0,1 12,16M12,10A2,2 0 0,1 14,12A2,2 0 0,1 12,14A2,2 0 0,1 10,12A2,2 0 0,1 12,10M12,4A2,2 0 0,1 14,6A2,2 0 0,1 12,8A2,2 0 0,1 10,6A2,2 0 0,1 12,4Z" />
					</svg>
				</span>
			</span>
		</article>
	</header>

	<section class="w-full">
		<ul class="flex justify-between items-center text-[10px] font-bold py-4">
			<li class="text-[#F17B7B] rounded-r-3xl border border-gray-400 border-solid">
				<span class="material-icons material-symbols-outlined p-2">videogame_asset</span>
			</li>
			<li class="text-[#F17B7B]">FRIENDS</li>
			<li class="text-[#1A73E9]">PROVIDERS</li>
			<li class="text-[#1A73E9]">MY CUSTOMERS</li>
			<li class="text-[#1A73E9]">DELIVERY</li>
			<li class="text-[#F17B7B] rounded-l-3xl border border-gray-400 border-solid">
				<span class="material-icons material-symbols-outlined p-2">checklist</span>
			</li>
		</ul>
	</section>

	<section class="p-2">
		<ul class="flex justify-between items-center text-center rounded-xl my-3 rounded-[12px] bg-[#FEFEFE]" style="box-shadow: rgba(0, 0, 0, 0.24) 0px 3px 8px;">
			<li class="text-sm font-normal rounded-xl text-white w-1/4 py-2 bg-[#F17B7B]">Stores</li>
			<li class="text-sm font-normal">Garages</li>
			<li class="text-sm font-normal">Employers</li>
			<li class="text-sm font-normal">Skills</li>
		</ul>
	</section>

	<section class="w-full my-4">
		{#if data && data.length > 0}
			{#each data as {id, name, time, picture, its, mtp}}
				<article class="flex items-center content-between px-2 my-3">
					<aside class="w-1/5 ">
						<img class="rounded-full h-12 w-12" src="{picture}" alt="">
					</aside>
					<div class="w-4/5 flex flex-col">
						<div class="flex justify-between items-center">
					<span class="font-bold leading-5 not-italic text-[15px]">
						{name}
					</span>
						<div class="flex items-center">
							<span class="text-gray-400 not-italic font-normal text-[15px] leading-5 mx-2">
								{time}
							</span>
							<span class="text-gray-400 mx-2">
								<svg xmlns="http://www.w3.org/2000/svg" height="24" viewBox="0 0 24 24" width="24">
									<path d="M0 0h24v24H0z" fill="none"/>
									<path d="M10 6L8.59 7.41 13.17 12l-4.58 4.59L10 18l6-6z"/>
								</svg>
							</span>
							</div>
						</div>
						<div class="text-gray-400 text-sm overflow-hidden truncate">
							Inquire to Seller: {its}
						</div>
						<div class="text-gray-400 text-sm overflow-hidden truncate">
							Makers Trust Purchase: {mtp}
						</div>
					</div>
				</article>
				<hr class="border-gray-400 border-t-1 my-2 right-0" />
			{/each}
		{/if}
	</section>

	<footer class="w-full">
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
</style>
