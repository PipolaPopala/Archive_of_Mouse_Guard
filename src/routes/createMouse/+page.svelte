<script>
	import CreateMouse from '../../components/createMouse/CreateMouse.svelte';
</script>

<svelte:head>
	<title>Create Mouse</title>
	<meta name="description" content="Create Mouse" />
</svelte:head>

<section>
	<h1>Создание персонажа</h1>
	<div>
		<CreateMouse />
	</div>
</section>

<style>
	div {
		display: flex;
		flex-direction: column;
	}
</style>
