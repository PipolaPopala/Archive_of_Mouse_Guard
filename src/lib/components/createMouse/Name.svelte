<script>
	import Modal from '../Modal.svelte';
	export let name;
	let showName = false;
	function openNameModal() {
		showName = true;
	}
	function closeNameModal() {
		showName = false;
	}
	let value = '';
	let nameArrayMan = [
		'Алгомuн',
		'Аррон',
		'Бuган',
		'Брэнд',
		'Вард',
		'Волмонд',
		'Гамлuн',
		'Гарнье',
		'Гарроу',
		'Грэхам',
		'Гурнu',
		'Джасnер',
		'Джозеф',
		'Каллен',
		'Келл',
		'Коннор',
		'Коул',
		'Курт',
		'Лэрд',
		'Нолан',
		'Сет',
		'Сuмон',
		'Слоун',
		'Тандер',
		'Тuзон',
		'Том',
		'ТреВор',
		'Фаолан',
		'Фuнн',
		'Фолкер',
		'Хэйл',
		'Хэнсон',
		'Энгус'
	];
	let nameArrayMale = [
		'Агнета',
		'Айби',
		'Баэлия',
		'Бринна',
		'Вера',
		'Гейла',
		'Дaлия',
		'Девона',
		'Джулия',
		'Жозефина',
		'Ингрид',
		'Квинн',
		'Кейли',
		'Кира',
		'Клоуви',
		'Лорель',
		'Лилли',
		'Лорелей',
		'Лунис',
		'Марена',
		'Миллисента',
		'Мойра',
		'Нола',
		'Розалина',
		'Рона',
		'Сибилла',
		'Сильвия',
		'Слоуни',
		'Сьерра',
		'Тарина',
		'Тинабель',
		'Эда',
		'Эделина'
	];
	function changeValue(elem) {
		value = elem;
	}
	function choiceName(value) {
		name = value;
	}
</script>

<button on:click={openNameModal}> {name || 'Выберите имя персонажу'} </button>
{#if showName}
	<Modal close={closeNameModal} title="Выберите имя и пол персонажа">
		<p>Выберите имя из предложенных, кликнув по нему, или придумайте своё</p>
		<p>Мужские имена:</p>
		{#each nameArrayMan as elem}
			<button type="button" on:click={() => changeValue(elem)}>{elem}</button>
		{/each}
		<p>Женские имена:</p>
		{#each nameArrayMale as elem}
			<button type="button" on:click={() => changeValue(elem)}>{elem}</button>
		{/each}

		<label>
			Введите своё имя
			<input type="text" bind:value />
		</label>

		<p>{value}</p>
		<button
			type="button"
			on:click={() => {
				choiceName(value);
				closeNameModal();
			}}>Подтвердить имя</button
		>
	</Modal>
{/if}

<style></style>
