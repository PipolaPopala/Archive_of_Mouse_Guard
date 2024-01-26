<script>
	import '../styles.css';
</script>

<header>
	<nav>
		<a href="/">Archive</a>
		<a href="/createMouse">Create Mouse</a>
		<a href="/profile">Profile</a>
		<a href="/authorization">Authorization</a>
	</nav>
</header>

<main>
	<slot />
</main>

<!-- import { fly } from 'svelte/transition'
in:fly={{ x: -500, duration: 500, delay: 500}} out:fly={{ x: 500, duration: 500 }} -->

<style>
	header {
		padding: 20px;
		display: flex;
		justify-content: center;
		align-items: center;
	}
	nav {
		width: 40%;
		display: flex;
		justify-content: center;
		align-items: center;
		justify-content: space-evenly;
	}
	main {
		padding: 20px;
	}
</style>
