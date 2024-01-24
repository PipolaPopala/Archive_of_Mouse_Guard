<script>
	export let choiceColorCloak;
	let value = '';
	let colors = [
		'Коричневый',
		'Русый',
		'Серый',
		'Чёрный',
		'Белый',
		'Рыжий'
	];
	function changeValue(elem) {
		value = elem;
	}
</script>

<p>Выберите цвет из предложенных, кликнув по нему, или придумайте свой</p>
{#each colors as elem}
	<button type="button" on:click={() => changeValue(elem)}>{elem}</button>
{/each}

<label>
	Введите свой цвет
	<input type="text" bind:value />
</label>

<p>{value}</p>
<button type="button" on:click={() => choiceColorCloak(value)}>Подтвердить цвет плаща</button>

<style></style>
