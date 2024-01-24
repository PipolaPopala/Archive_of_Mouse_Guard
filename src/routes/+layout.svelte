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

<style>
  header{
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
