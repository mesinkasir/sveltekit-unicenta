<script context="module">
    import { onMount } from 'svelte'
	import { browser, dev } from '$app/env';
	export const hydrate = dev;
	export const router = browser;
	export const prerender = true;    
</script>

<svelte:head>
	<title>Categories Products List</title>
</svelte:head>
<script>
    
    const apiURL = 'http://localhost/API/conn.php';
    let data = [];onMount(async function() {const response = await fetch(apiURL);data = await response.json();});
</script>
<div class="content">
	<h1>Categories Products List</h1>

<div class="row p-3">
	{#each data as item}
	<main class="col-6 p-3 border border-secondary p-md-5 text-center">
		<p>
		 {item.name}
	</p>
</main>
		{/each}
</div>
</div>