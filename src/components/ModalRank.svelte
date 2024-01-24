<script>
	export let choiceRank;
	let value = '';
	function changeValue(elem) {
		value = elem;
	}
</script>

<p>Выберите ранг персонажа</p>

<button type="button" on:click={() => changeValue('Лапа помощи')}>Лапа помощи</button>
<button type="button" on:click={() => changeValue('Страж')}>Страж</button>
<button type="button" on:click={() => changeValue('Патрульный')}>Патрульный</button>
<button type="button" on:click={() => changeValue('Лидер патруля')}>Лидер патруля</button>
<button type="button" on:click={() => changeValue('Капитан')}>Капитан</button>

<p>{value}</p>
<button type="button" on:click={() => choiceRank(value)}>Подтвердить выбор ранга</button>

<style></style>
