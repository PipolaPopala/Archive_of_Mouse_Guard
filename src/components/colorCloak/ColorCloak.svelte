<script>
	import Modal from '../Modal.svelte';
	import ModalColorCloak from './ModalColorCloak.svelte';
	export let choiceColorCloak;
	let showColorCloak = false;
	function openColorCloakModal() {
		showColorCloak = true;
	}
	function closeColorCloakModal() {
		showColorCloak = false;
	}
</script>

<button on:click={openColorCloakModal}> Выберите цвет плаща </button>
{#if showColorCloak}
	<Modal close={closeColorCloakModal} title="Выберите цвет плаща">
		<ModalColorCloak {choiceColorCloak} {closeColorCloakModal}/>
	</Modal>
{/if}

<style></style>
