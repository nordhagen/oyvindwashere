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
	<title>About</title>
</svelte:head>

<div class="content">
	<h1>Here's me</h1>
	<p>My name is Øyvind Nordhagen and I'm a street photographer based in Oslo, Norway. </p>
	<p>I got my first camera when I was 13 years old and have been making pictures ever since (a <a href="https://www.lomography.com/magazine/228380-minolta-dynax-3000i-the-slr-for-lazy-photographers">Minolta Dynax 3000i </a> if you're interested). </p>
</div>

<style>
	.content {
		width: 100%;
		max-width: var(--column-width);
		margin: var(--column-margin-top) auto 0 auto;
	}
</style>
