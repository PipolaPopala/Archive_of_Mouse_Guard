<script>
	import Modal from '../../components/Modal.svelte';
	import ModalName from '../../components/ModalName.svelte';
	import ModalRank from '../../components/ModalRank.svelte';
	import ModalBirth from '../../components/ModalBirth.svelte';
	import ModalExperience from '../../components/ModalExperience.svelte';
	import ModalNature from '../../components/ModalNature.svelte';
	import ModalKnowledge from '../../components/ModalKnowledge.svelte';
	import ModalTraits from '../../components/ModalTraits.svelte';
	import ModalColorWool from '../../components/ModalColorWool.svelte';
	import ModalColorCloak from '../../components/ModalColorCloak.svelte';

	let concept = '';

	let name = '';
	let showName = false;
	function openNameModal() {
		showName = true;
	}
	function closeNameModal() {
		showName = false;
	}
	function choiceName(value) {
		name = value;
		showName = false;
	}

	let rank = '';
	let showRank = false;
	function openRankModal() {
		showRank = true;
	}
	function closeRankModal() {
		showRank = false;
	}
	function choiceRank(value) {
		rank = value;
		showRank = false;
	}

	let birthplace = {};
	let showBirth = false;
	function openBirthModal() {
		showBirth = true;
	}
	function closeBirthModal() {
		showBirth = false;
	}
	function choiceBirth(value) {
		birthplace = value;
		showBirth = false;
	}

	let experience = [];
	let showExperience = false;
	function openExperienceModal() {
		showExperience = true;
	}
	function closeExperienceModal() {
		showExperience = false;
	}
	function choiceExperience(value) {
		experience = value;
		showExperience = false;
	}

	let nature = 3;
	let showNature = false;
	function openNatureModal() {
		showNature = true;
	}
	function closeNatureModal() {
		showNature = false;
	}
	function choiceNature(value) {
		nature = value;
		showNature = false;
	}

	let knowledge = [];
	let showKnowledge = false;
	function openKnowledgeModal() {
		showKnowledge = true;
	}
	function closeKnowledgeModal() {
		showKnowledge = false;
	}
	function choiceKnowledge(value) {
		knowledge = value;
		showKnowledge = false;
	}

	let traits = [];
	let showTraits = false;
	function openTraitsModal() {
		showTraits = true;
	}
	function closeTraitsModal() {
		showTraits = false;
	}
	function choiceTraits(value) {
		traits = value;
		showTraits = false;
	}

	let colorWool = '';
	let showColorWool = false;
	function openColorWoolModal() {
		showColorWool = true;
	}
	function closeColorWoolModal() {
		showColorWool = false;
	}
	function choiceColorWool(value) {
		colorWool = value;
		showColorWool = false;
	}

	let colorCloak = '';
	let showColorCloak = false;
	function openColorCloakModal() {
		showColorCloak = true;
	}
	function closeColorCloakModal() {
		showColorCloak = false;
	}
	function choiceColorCloak(value) {
		colorCloak = value;
		showColorCloak = false;
	}

	let parents = [];
	let master = '';
	let mentor = '';
	let friend = '';
	let enemy = '';
	let conviction = '';
	let instinct = '';
	let goal = '';
	let equipment = '';
</script>

<svelte:head>
	<title>Create Mouse</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section>
	<h1>Создание персонажа</h1>
	<div>
		<label>
			<p>Концепция персонажа</p>
			<textarea name="" cols="30" rows="3" bind:value={concept}></textarea>
		</label>
		<p>{concept}</p>

		<button on:click={openNameModal}> Выберите имя и пол персонажа </button>
		<p>{name}</p>
		{#if showName}
			<Modal close={closeNameModal} title="Выберите имя и пол персонажа">
				<ModalName {choiceName} />
			</Modal>
		{/if}

		<button on:click={openRankModal}> Выберите ранг персонажа </button>
		<p>{rank}</p>
		{#if showRank}
			<Modal close={closeRankModal} title="Выберите ранг персонажа">
				<ModalRank {choiceRank} />
			</Modal>
		{/if}

		<button on:click={openBirthModal}> Выберите место рождения персонажа </button>
		<p>{birthplace.name}</p>
		{#if showBirth}
			<Modal close={closeBirthModal} title="Выберите место рождения персонажа">
				<ModalBirth {choiceBirth} />
			</Modal>
		{/if}

		<button on:click={openExperienceModal}> Жизненный опыт персонажа </button>
		<p>Где-то здесь разместить навыки</p>
		<p>{experience}</p>
		{#if showExperience}
			<Modal close={closeExperienceModal} title="Определите жизненный опыт персонажа">
				<ModalExperience {choiceExperience} />
			</Modal>
		{/if}

		<button on:click={openNatureModal}> Мышиная природа </button>
		<p>{nature}</p>
		{#if showNature}
			<Modal close={closeNatureModal} title="Определите мышиную природу">
				<ModalNature {choiceNature} />
			</Modal>
		{/if}

		<button on:click={openKnowledgeModal}> Имеющиеся знания </button>
		<p>{knowledge}</p>
		{#if showKnowledge}
			<Modal close={closeKnowledgeModal} title="Определите имеющиеся знания">
				<ModalKnowledge {choiceKnowledge} />
			</Modal>
		{/if}

		<button on:click={openTraitsModal}> Мышиные черты </button>
		<p>{traits}</p>
		{#if showTraits}
			<Modal close={closeTraitsModal} title="Определите мышиные черты">
				<ModalTraits {choiceTraits} />
			</Modal>
		{/if}

		<button on:click={openColorWoolModal}> Выберите цвет шёрстки </button>
		<p>{colorWool}</p>
		{#if showColorWool}
			<Modal close={closeColorWoolModal} title="Выберите цвет шёрстки">
				<ModalColorWool {choiceColorWool} />
			</Modal>
		{/if}

		<button on:click={openColorCloakModal}> Выберите цвет плаща </button>
		<p>{colorCloak}</p>
		{#if showColorCloak}
			<Modal close={closeColorCloakModal} title="Выберите цвет плаща">
				<ModalColorCloak {choiceColorCloak} />
			</Modal>
		{/if}

		<label>
			<p>Назовите родителей</p>
			<textarea name="" cols="30" rows="3" bind:value={parents}></textarea>
		</label>
		<p>{parents}</p>

		<label>
			<p>Назовите мастера</p>
			<textarea name="" cols="30" rows="3" bind:value={master}></textarea>
		</label>
		<p>{master}</p>

		<label>
			<p>Назовите наставника</p>
			<textarea name="" cols="30" rows="3" bind:value={mentor}></textarea>
		</label>
		<p>{mentor}</p>

		<label>
			<p>Назовите друга</p>
			<textarea name="" cols="30" rows="3" bind:value={friend}></textarea>
		</label>
		<p>{friend}</p>

		<label>
			<p>Назовите врага</p>
			<textarea name="" cols="30" rows="3" bind:value={enemy}></textarea>
		</label>
		<p>{enemy}</p>

		<label>
			<p>Убеждение</p>
			<textarea name="" cols="30" rows="3" bind:value={conviction}></textarea>
		</label>
		<p>{conviction}</p>

		<label>
			<p>Инстинкты</p>
			<textarea name="" cols="30" rows="3" bind:value={instinct}></textarea>
		</label>
		<p>{instinct}</p>

		<label>
			<p>Цели</p>
			<textarea name="" cols="30" rows="3" bind:value={goal}></textarea>
		</label>
		<p>{goal}</p>

		<label>
			<p>Снаряжение</p>
			<textarea name="" cols="30" rows="3" bind:value={equipment}></textarea>
		</label>
		<p>{equipment}</p>

		<p>Где-то разместить проверочные баллы, баллы судьбы и баллы личности</p>
	</div>
</section>

<style>
	div {
		display: flex;
		flex-direction: column;
	}
</style>
