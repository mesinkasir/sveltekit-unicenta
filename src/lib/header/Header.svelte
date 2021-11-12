<script>
	import { page } from '$app/stores';
	import logo from './svelte-logo.svg';
</script>
	<nav class="navbar navbar-expand-lg navbar-light bg-light border-bottom border-secondary">
		<div class="container-fluid">
		  <a class="navbar-brand" href="/">	<img class="img-fluid" width="40" src={logo} alt="SvelteKit" /></a>
		  <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
			<span class="navbar-toggler-icon"></span>
		  </button>
		  <div class="collapse navbar-collapse justify-content-end" id="navbarNav">
			<ul class="navbar-nav p-1">
			<li class="nav-item" class:active={$page.path === '/index'}><a class="nav-link" sveltekit:prefetch href="/">Home</a></li>
			<li class="nav-item"class:active={$page.path === '/about'}><a class="nav-link" sveltekit:prefetch href="/about">About</a></li>
			<li class="nav-item"class:active={$page.path === '/cat'}><a class="nav-link" sveltekit:prefetch href="/cat">Categories</a></li>
			<li class="nav-item"class:active={$page.path === '/cost'}><a class="nav-link" sveltekit:prefetch href="/cost">Cost</a></li>
			<li class="nav-item"class:active={$page.path === '/price'}><a class="nav-link" sveltekit:prefetch href="/price">Sell</a></li>
			<li class="nav-item"class:active={$page.path === '/user'}><a class="nav-link" sveltekit:prefetch href="/user">User</a></li>
			<li class="nav-item"class:active={$page.path === '/cash'}><a class="nav-link" sveltekit:prefetch href="/cash">Cash Flow</a></li>
			<li class="nav-item"class:active={$page.path === '/close'}><a class="nav-link" sveltekit:prefetch href="/close">Close Cash</a></li>
			<li class="nav-item"class:active={$page.path === '/todos'}><a class="nav-link" sveltekit:prefetch href="/todos">Todos</a></li>
			<li class="nav-item"><a class="nav-link btn btn-dark text-white" href="https://github.com/mesinkasir/sveltekit-unicenta">Github</a></li>
		</ul>
	</div>
</div>
</nav>