<script>
	import Modal from '../Modal.svelte';
	import ModalKnowledge from './ModalKnowledge.svelte';
	export let choiceKnowledge;
	let showKnowledge = false;
	function openKnowledgeModal() {
		showKnowledge = true;
	}
	function closeKnowledgeModal() {
		showKnowledge = false;
	}
</script>

<button on:click={openKnowledgeModal}> Имеющиеся знания </button>
{#if showKnowledge}
	<Modal close={closeKnowledgeModal} title="Определите имеющиеся знания">
		<ModalKnowledge {choiceKnowledge} {closeKnowledgeModal}/>
	</Modal>
{/if}

<style></style>
