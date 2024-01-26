<script>
	import Modal from '../Modal.svelte';
	import ModalTraits from './ModalTraits.svelte';
	export let choiceTraits;
	let showTraits = false;
	function openTraitsModal() {
		showTraits = true;
	}
	function closeTraitsModal() {
		showTraits = false;
	}
</script>

<button on:click={openTraitsModal}> Мышиные черты </button>
{#if showTraits}
	<Modal close={closeTraitsModal} title="Определите мышиные черты">
		<ModalTraits {choiceTraits} {closeTraitsModal}/>
	</Modal>
{/if}

<style></style>
