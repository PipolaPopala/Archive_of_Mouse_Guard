<script>
	import Modal from '../Modal.svelte';
	import ModalRank from './ModalRank.svelte';
	export let choiceRank;
	let showRank = false;
	function openRankModal() {
		showRank = true;
	}
	function closeRankModal() {
		showRank = false;
	}
</script>

<button on:click={openRankModal}> Выберите ранг персонажа </button>
{#if showRank}
	<Modal close={closeRankModal} title="Выберите ранг персонажа">
		<ModalRank {choiceRank} {closeRankModal}/>
	</Modal>
{/if}

<style></style>
