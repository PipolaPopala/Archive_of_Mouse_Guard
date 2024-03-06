<script>
	import '../styles.css';
</script>

<header>
	<nav>
		<a href="/">Архив</a>
		<a href="/createMouse">Создание персонажа</a>
		<a href="/profile">Профиль пользователя</a>
		<a href="/authorization">Авторизация</a>
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
