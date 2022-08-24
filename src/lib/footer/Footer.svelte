<script lang="ts">
    import { page } from '$app/stores';
    let active: string = '/';
    $: {
        active = $page.url.pathname;
        console.log(active);
    }
</script>

<header class="fixed w-full bottom-0 left-0 ct-shadow ">
    <nav class="">
        <!-- <ul>
            <li class:active={$page.url.pathname === '/'}><a sveltekit:prefetch href="/">Home</a></li>
            <li class:active={$page.url.pathname === '/about'}>
                <a sveltekit:prefetch href="/about">About</a>
            </li>
            <li class:active={$page.url.pathname === '/todos'}>
                <a sveltekit:prefetch href="/todos">Todos</a>
            </li>
        </ul> -->
        <ul class="flex flex-row uppercase justify-center text-center text-gray-700 overflow-x-auto">
            <li class={`${active.indexOf('home') >= 0 ? 'text-blue-600' : ''} m-auto p-3`}>
                <a href="/home"
                ><span class="material-icons material-symbols-outlined"> shopping_cart </span> <br /><span
                        class="text-xs">Cetech</span
                ></a
                >
            </li>
            <li class={`${active.indexOf('delivery') >= 0 ? 'text-blue-600' : ''} m-auto p-3`}>
                <a href="/"
                ><span class="material-icons material-symbols-outlined"> import_contacts </span>
                    <br /><span class="text-xs">Delivery</span></a
                >
            </li>
            <li class={`${active.indexOf('earn') >= 0 ? 'text-blue-600' : ''} m-auto p-3`}>
                <a href="/"
                ><span class="material-icons material-symbols-outlined"> add_circle </span> <br /><span
                        class="text-xs">Earn</span
                ></a
                >
            </li>
            <li class={`${active.indexOf('mall') >= 0 ? 'text-blue-600' : ''} m-auto p-3`}>
                <a href="/"
                ><span class="material-icons material-symbols-outlined"> shopping_bag </span> <br /><span class="text-xs"
                >Mall</span
                ></a
                >
            </li>
            <li class={`${active.indexOf('dwta') >= 0 ? 'text-blue-600' : ''} m-auto p-3`}>
                <a href="/"><span class="material-icons material-symbols-outlined"> laptop </span><br /><span class="text-xs">DWTA</span></a>
            </li>
            <li class={` m-auto p-3`}>
				<span class="ml-3"
                ><span class="material-icons material-symbols-outlined"> menu </span> <br /><span class="text-xs"
                >More</span
                ></span
                >
            </li>
        </ul>
    </nav>
</header>
