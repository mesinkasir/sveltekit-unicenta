<script context="module">
    import { onMount } from 'svelte'
	import { browser, dev } from '$app/env';
	export const hydrate = dev;
	export const router = browser;
	export const prerender = true;    
</script>

<svelte:head>
	<title>Product Price Cost</title>
</svelte:head>
<script>
    
    const apiURL = 'http://localhost/API/connect.php';
    let data = [];onMount(async function() {const response = await fetch(apiURL);data = await response.json();});
</script>
<div class="content">
	<h1>Product Price Cost</h1>

<div class="row p-3">
	{#each data as item}
	<main class="col-md-4 col-12 p-3 border-secondary p-md-5 border-secondary border text-center">
		<p>
        Barcode : {item.code}<br/>
		Item : {item.name}<br/>
		Price : {item.pricebuy}
	</p>
</main>
		{/each}
</div>
</div>