<script>
	import Modal from '../Modal.svelte';
	import ModalHome from './ModalHome.svelte';
	export let choiceHome;
	let showHome = false;
	function openHomeModal() {
		showHome = true;
	}
	function closeHomeModal() {
		showHome = false;
	}
</script>

<button on:click={openHomeModal}> Выберите место рождения персонажа </button>
{#if showHome}
	<Modal close={closeHomeModal} title="Выберите место рождения персонажа">
		<ModalHome {choiceHome} {closeHomeModal}/>
	</Modal>
{/if}

<style></style>
