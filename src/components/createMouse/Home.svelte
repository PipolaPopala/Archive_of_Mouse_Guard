<script>
	import Modal from '../Modal.svelte';
	export let home;
	let showHome = false;
	function openHomeModal() {
		showHome = true;
	}
	function closeHomeModal() {
		showHome = false;
	}
	let value = { name: '', description: '', skills: [], traits: [] };
	function changeValue(elem) {
		value = elem;
	}
	function choiceHome(value) {
		home = value;
	}
	let birthplaceArray = [
		{
			name: 'Древоград',
			description: '- шумный рабочий городок.',
			skills: ['Гончар', 'Плотник', 'Стекольщик'],
			traits: ['Золотые лапы']
		},
		{
			name: 'Кремнержавь',
			description:
				'- когда-то большой город, а теперь бедный городок, в котором хорошо относятся к Мышиной Страже.',
			skills: ['Кузнец', 'Разнорабочий'],
			traits: ['Безрассудный', 'Решительный']
		},
		{
			name: 'Локхэйвен',
			description: '- цытадель Мышиной Стражи.',
			skills: ['Оружейник', 'Ткач'],
			traits: ['Доверие Стражи', 'Щедрый']
		},
		{
			name: 'Меднолесье',
			description:
				'- один из старейших городов, в котором расположен один из двух рудников Территорий, где добывают металл.',
			skills: ['Кузнец', 'Торгаш'],
			traits: ['Независимый']
		},
		{
			name: 'Моховяз',
			description: '- некогда процветающий город, известный целебным мхом.',
			skills: ['Плотник', 'Сборщик'],
			traits: ['Бдительный']
		},
		{
			name: 'Песчаный дом',
			description: '- жители этого города предпочитают добрствовать по ночам.',
			skills: ['Наблюдатель за погодой', 'Стекольщик'],
			traits: ['Сова', 'Тихий']
		},
		{
			name: 'Плющи',
			description: '- известен своими пекарями и хлебом.',
			skills: ['Пекарь', 'Сборщик'],
			traits: ['Трудолюбивый']
		},
		{
			name: 'Подъельник',
			description: '- прославлен своими учёными, лекарствами и отваром для поддержания границы.',
			skills: ['Знаток зверей', 'Учёный'],
			traits: ['Дотошный', 'Рациональный']
		},
		{
			name: 'Порт-Сумах',
			description:
				'- маленький шумный портовый городок, расположенный между Темновольем и Ржаволистом.',
			skills: ['Корабел', 'Наблюдатель за погодой'],
			traits: ['Крепкий', 'Метеочувствительный']
		},
		{
			name: 'Сланцевая нора',
			description: '- простой городок, славящийся своими напитками.',
			skills: ['Каменщик', 'Мельник', 'Сборщик'],
			traits: ['Открытый']
		},
		{
			name: 'Травоозёрье',
			description:
				'- город, расположенный на берегу озера. Его жители известны воинственным нравом.',
			skills: ['Военный', 'Насекомовод'],
			traits: ['Защитник', 'Проворный']
		},
		{
			name: 'Виндзельм',
			description: '',
			skills: [],
			traits: []
		},
		{
			name: 'Волчий Клык',
			description: '',
			skills: [],
			traits: []
		},
		{
			name: 'Гальбрук',
			description: '',
			skills: [],
			traits: []
		},
		{
			name: 'Гилов Обет',
			description: '',
			skills: [],
			traits: []
		},
		{
			name: 'Доридар',
			description: '',
			skills: [],
			traits: []
		},
		{
			name: 'Железнолесье',
			description: '',
			skills: [],
			traits: []
		},
		{
			name: 'Зябкий',
			description: '',
			skills: [],
			traits: []
		},
		{
			name: 'Калогеро',
			description: '',
			skills: [],
			traits: []
		},
		{
			name: 'Камнекрепь',
			description: '',
			skills: [],
			traits: []
		},
		{
			name: 'Кленовая Гавань',
			description: '',
			skills: [],
			traits: []
		},
		{
			name: 'Корневал',
			description: '',
			skills: [],
			traits: []
		},
		{
			name: 'Ржаволист',
			description: '',
			skills: [],
			traits: []
		},
		{
			name: 'Темноводье',
			description: '',
			skills: [],
			traits: []
		},
		{
			name: 'Чёрный Утёс',
			description: '',
			skills: [],
			traits: []
		},
		{
			name: 'Яблочный Дом',
			description: '',
			skills: [],
			traits: []
		},
		{
			name: 'Белая Сосна',
			description: '',
			skills: [],
			traits: []
		},
		{
			name: 'Берёзовый Поток',
			description: '',
			skills: [],
			traits: []
		},
		{
			name: 'Вязолесье',
			description: '',
			skills: [],
			traits: []
		},
		{
			name: 'Разнотрав',
			description: '',
			skills: [],
			traits: []
		},
		{
			name: 'Дубовый Гай',
			description: '',
			skills: [],
			traits: []
		},
		{
			name: 'Рассветная Скала',
			description: '',
			skills: [],
			traits: []
		},
		{
			name: 'Одинокая Сосна',
			description: '',
			skills: [],
			traits: []
		},
		{
			name: 'Роща Лилли',
			description: '',
			skills: [],
			traits: []
		},
		{
			name: 'Свиль',
			description: '',
			skills: [],
			traits: []
		},
		{
			name: 'Чертополохи',
			description: '',
			skills: [],
			traits: []
		}
	];
</script>

<button on:click={openHomeModal}> {home.name || 'Выберите место рождения персонажа'}  </button>
{#if showHome}
	<Modal close={closeHomeModal} title="Выберите место рождения персонажа">
		<p>
			(здесь можно расположить всю карту Мышиных Территорий, и подтвечивать города на ней. При
			наведении, раскрывается окошко с информацией про этот город, при наведении на черты, так же
			откроется подробное описание черты. Кликнув на город, информация о нём оказывается ниже, там
			же стоит выбрать навыки и черту, после чего можно подтвердить выбор.)
		</p>

		{#each birthplaceArray as town}
			<button type="button" on:click={() => changeValue(town)}>
				<p>{`${town.name} ${town.description}`}</p>
				<p>Навыки жителей: {town.skills.join(', ')}</p>
				<p>Черты жителей: {town.traits.join(', ')}</p>
			</button>
		{/each}

		<p>{value.name}</p>
		<button
			type="button"
			on:click={() => {
				choiceHome(value);
				closeHomeModal();
			}}>Подтвердить выбор места рождения</button
		>
	</Modal>
{/if}

<style></style>
