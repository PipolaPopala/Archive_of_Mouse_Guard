<script>
	import Modal from '../Modal.svelte';
	import ModalColorFur from './ModalColorFur.svelte';
	export let choiceColorFur;
	let showColorFur = false;
	function openColorFurModal() {
		showColorFur = true;
	}
	function closeColorFurModal() {
		showColorFur = false;
	}
</script>

<button on:click={openColorFurModal}> Выберите цвет шёрстки </button>
{#if showColorFur}
	<Modal close={closeColorFurModal} title="Выберите цвет шёрстки">
		<ModalColorFur {choiceColorFur} {closeColorFurModal}/>
	</Modal>
{/if}

<style></style>
