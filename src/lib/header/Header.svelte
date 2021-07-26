<script lang="ts">
	import { page } from '$app/stores';
	import logo from './oyvindnordhagen-black.svg';
</script>

<header>
	<div class="logo">
		<a href="https://oyvindwashere.com">
			<img src={logo} alt="Øyvind Nordhagen" />
		</a>
	</div>

	<nav>
		<ul>
			<li class:active={$page.path === '/'}><a sveltekit:prefetch href="/">Gallery</a></li>
			<li class:active={$page.path === '/blog'}><a sveltekit:prefetch href="/blog">Blog</a></li>
			<li class:active={$page.path === '/about'}><a sveltekit:prefetch href="/about">About</a></li>
		</ul>
	</nav>
</header>

<style>
	header {
		display: flex;
		justify-content: space-between;
	}
	
	.logo {
		width: 26rem;
		height: 3rem;
		padding: 2rem;
	}

	.logo a {
		display: flex;
		align-items: center;
		justify-content: center;
	}

	.logo img {
		width: 100%;
		object-fit: contain;
	}

	nav {
		display: flex;
		justify-content: center;
	}

	ul {
		position: relative;
		padding: 0;
		margin: 0;
		display: flex;
		justify-content: center;
		align-items: center;
		list-style: none;
		height: 100%;
	}

	li {
		position: relative;
	}

	nav a {
		display: flex;
		height: 100%;
		align-items: center;
		padding: 0 1em;
		color: var(--heading-color);
		font-weight: 400;
		font-size: 1.6rem;
		text-transform: uppercase;
		letter-spacing: 10%;
		text-decoration: none;
		transition: color 0.2s linear;
	}

	a:hover, li.active a {
		color: var(--accent-color);
	}
</style>
