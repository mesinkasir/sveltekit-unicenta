<script context="module">
    import { onMount } from 'svelte'
	import { browser, dev } from '$app/env';
	export const hydrate = dev;
	export const router = browser;
	export const prerender = true;    
</script>

<svelte:head>
	<title>Cash Flow</title>
</svelte:head>
<script>
    
    const apiURL = 'http://localhost/API/pp.php';
    let data = [];onMount(async function() {const response = await fetch(apiURL);data = await response.json();});
          
</script>
<div class="content">
	<h1>Cash Flow</h1>

<div class="row p-3">
	{#each data as item}
	<main class="col-md-6 col-12 p-3 border-secondary p-md-5 border-secondary border text-center">
		<p>
        Type : {item.payment}<br/>
		Total : {item.total}<br/>
		Tendered : {item.tendered}<br/>
       </p>
</main>
		{/each}
</div>
</div>