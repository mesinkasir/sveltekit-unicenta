<script context="module">
	import { browser, dev } from '$app/env';

	// we don't need any JS on this page, though we'll load
	// it in dev so that we get hot module replacement...
	export const hydrate = dev;

	// ...but if the client-side router is already loaded
	// (i.e. we came here from elsewhere in the app), use it
	export const router = browser;

	// since there's no dynamic data here, we can prerender
	// it so that it gets served as a static asset in prod
	export const prerender = true;
</script>

<svelte:head>
	<title>Unicenta web apps</title>
</svelte:head>

<div class="content row">
	<h1>Unicenta Web App</h1>
	<div class="col-12 col-md-12 p-3">
        <div class="ratio ratio-16x9">
            <iframe src="https://www.youtube.com/embed/aEVYUeubfJk" title="Unicenta website application" class="rounded" allowfullscreen></iframe>
          </div>
          <p>This time for build your modern website and integration with unicentapos desktop apps.</p>
        </div>	
</div>
