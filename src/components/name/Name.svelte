<script>
	import Modal from '../Modal.svelte';
	import ModalName from './ModalName.svelte';
	export let choiceName;
	let showName = false;
	function openNameModal() {
		showName = true;
	}
	function closeNameModal() {
		showName = false;
	}
</script>

<button on:click={openNameModal}> Выберите имя и пол персонажа </button>
{#if showName}
	<Modal close={closeNameModal} title="Выберите имя и пол персонажа">
		<ModalName {choiceName} {closeNameModal}/>
	</Modal>
{/if}

<style></style>
