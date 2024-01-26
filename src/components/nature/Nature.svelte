<script>
	import Modal from "../Modal.svelte";
	import ModalNature from "./ModalNature.svelte";
	export let choiceNature;
	let showNature = false;
	function openNatureModal() {
		showNature = true;
	}
	function closeNatureModal() {
		showNature = false;
	}
</script>

<button on:click={openNatureModal}> Мышиная природа </button>
{#if showNature}
	<Modal close={closeNatureModal} title="Определите мышиную природу">
		<ModalNature {choiceNature} {closeNatureModal}/>
	</Modal>
{/if}

<style></style>
