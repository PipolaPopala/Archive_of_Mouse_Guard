<script>
	import Modal from '../Modal.svelte';
	import ModalSkills from './ModalSkills.svelte';
	export let choiceSkills;
	let showSkills = false;
	function openSkillsModal() {
		showSkills = true;
	}
	function closeSkillsModal() {
		showSkills = false;
	}
</script>

<button on:click={openSkillsModal}> Жизненный опыт персонажа </button>
<p>Где-то здесь разместить навыки</p>
{#if showSkills}
	<Modal close={closeSkillsModal} title="Определите жизненный опыт персонажа">
		<ModalSkills {choiceSkills} {closeSkillsModal}/>
	</Modal>
{/if}

<style></style>
