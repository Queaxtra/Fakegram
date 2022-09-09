<script>
    import Router, {location, link} from 'svelte-spa-router';
    import Home from '../lib/Home.svelte';
    import Create from '../lib/Create.svelte';
</script>

<div class="w-auto h-16 bg-gray-200 drop-shadow-md">
    <h2 class="relative ml-5 top-3.5 text-2xl font-extrabold">Fakegram</h2>
    <ul class="block relative -top-3.5 text-center invisible md:visible sm:visible">
        <li class="inline m-3">
            <a class="opacity-70 hover:opacity-100" href="/"><i class="fa-solid fa-house"></i> Home</a>
        </li>
        <li class="inline m-3">
            <a class="opacity-70 hover:opacity-100" href="/create" use:link><i class="fa-solid fa-plus"></i> Create Post</a>
        </li>
    </ul>
    <div class="float-right visible md:invisible sm:invisible">
        <div class="relative dropdown dropdown-end -top-10 right-5 w-9 h-9 bg-gray-100 drop-shadow-md rounded">
            <label tabindex="0">
                <i class="relative left-1/2 -translate-x-1/2 text-lg top-1 text-gray-600 fa-solid fa-bars"></i>
            </label>
            <ul tabindex="0" class="relative top-14 dropdown-content menu p-2 shadow bg-white rounded w-52">
                <li>
                    <a class="opacity-70 hover:opacity-100" href="/"><i class="fa-solid fa-house"></i> Home</a>
                </li>
                <li>
                    <a class="opacity-70 hover:opacity-100" href="/create" use:link><i class="fa-solid fa-plus"></i> Create Post</a>
                </li>
            </ul>
        </div>
    </div>
</div>

<Router routes={{
    '/': Home,
    '/create': Create
}} />