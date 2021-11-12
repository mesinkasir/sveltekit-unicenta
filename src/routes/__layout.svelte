<script>
	import Header from '$lib/header/Header.svelte';
	import '../app.css';
</script>

<Header />

<main class="container  p-3">
	<slot />
</main>

<footer class="p-3 text-center">
	<p><small>this project present by <a href="https://axcora.com" class="text-secondary">axcora technology</a> develope using <a href="https://kit.svelte.dev" class="text-secondary">kit.svelte.dev</a></small></p>
</footer>
