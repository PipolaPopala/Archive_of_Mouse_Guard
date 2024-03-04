<script>
	import Modal from '../Modal.svelte';
	export let knowledge;
	let showKnowledge = false;
	function openKnowledgeModal() {
		showKnowledge = true;
	}
	function closeKnowledgeModal() {
		showKnowledge = false;
	}
	let value = [];
	function changeValue(elem) {
		value = [...value, elem];
	}
	function choiceKnowledge(value) {
		knowledge = value;
	}
	let knowledgeArray = [
		'безделушках и украшениях',
		'болотах',
		'внезапных паводках',
		'войне',
		'восстаниях',
		'высокой траве',
		'голоде',
		'границе',
		'грозах',
		'грязи',
		'дефиците',
		'дикой стране',
		'диче',
		'дождях',
		'дорогах',
		'ездовых животных',
		'ежевике',
		'засухе',
		'звездах',
		'зерне',
		'змеях',
		'каменистой местности',
		'ласках',
		'лесе',
		'лесных пожарах',
		'ловушках',
		'льде',
		'маршрутах',
		'медицине',
		'метелях',
		'мхе',
		'морозах',
		'наплывах жары',
		'не по сезону теплой погоде',
		'ночном времени суток',
		'оружии и броне',
		'орехах',
		'осенних грозах',
		'открытой местности',
		'палой листве',
		'птицах',
		'подлеске',
		'побережьях',
		'праздниках',
		'преступности',
		'прибрежных водах',
		'приливах и отливах',
		'прудах и озерах',
		'почте',
		'пчеловодстве',
		'растениеводстве',
		'реках и ручьях',
		'ремесленниках',
		'рецептах',
		'ручном труде',
		'сильном похолодании',
		'следах',
		'снегопадах',
		'снежных бурях',
		'снежном покрове',
		'сопровождении',
		'Тёмном Вереске',
		'тёплой и жаркой погоде',
		'травах',
		'транспортных средствах',
		'тумане',
		'туннелях',
		'укрытиях',
		'урожае',
		'хищниках',
		'холоде',
		'обморожении',
		'шипах и колючках',
		'щетках и кистях',
		'щитах',
		'эпидемиях',
		'ядах',
		'ясной и теплой погоде'
	];
	let knowledgeArrayIntern = ['Кодексе Стражи', 'Сказания о Страже'];
	let knowledgeArrayKapitans = ['Локхейвене', 'Матриархе Стражи'];
</script>

<button on:click={openKnowledgeModal}> Имеющиеся знания </button>
{#if showKnowledge}
	<Modal close={closeKnowledgeModal} title="Определите имеющиеся знания">
		<p>Выберите знания персонажа</p>

		{#each knowledgeArray as knowledge}
			<button type="button" on:click={() => changeValue(knowledge)}>
				{knowledge}
			</button>
		{/each}
		<br />
		{#each knowledgeArrayIntern as knowledge}
			<button type="button" on:click={() => changeValue(knowledge)}>
				{knowledge}
			</button>
		{/each}
		<br />
		{#each knowledgeArrayKapitans as knowledge}
			<button type="button" on:click={() => changeValue(knowledge)}>
				{knowledge}
			</button>
		{/each}

		<p>{value}</p>
		<button
			type="button"
			on:click={() => {
				choiceKnowledge(value);
				closeKnowledgeModal();
			}}>Подтвердить выбор знаний</button
		>
	</Modal>
{/if}

<style></style>
