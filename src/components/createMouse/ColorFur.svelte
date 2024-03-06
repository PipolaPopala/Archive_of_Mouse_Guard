<script>
	import Modal from '../Modal.svelte';
	export let colorFur;
	let showColorFur = false;
	function openColorFurModal() {
		showColorFur = true;
	}
	function closeColorFurModal() {
		showColorFur = false;
	}
	let value = '';
	let colors = ['Коричневый', 'Русый', 'Серый', 'Чёрный', 'Белый', 'Рыжий'];
	function changeValue(elem) {
		value = elem;
	}
	function choiceColorFur(value) {
		colorFur = value;
	}
</script>

<button on:click={openColorFurModal}> {colorFur || 'Выберите цвет шёрстки'} </button>
{#if showColorFur}
	<Modal close={closeColorFurModal} title="Выберите цвет шёрстки">
		<p>
			(забавно было бы нарисовать некий эскиз мышки, и, при выборе цвета у неё меняется шёрстка)
		</p>

		<p>Выберите цвет из предложенных, кликнув по нему, или придумайте свой</p>
		{#each colors as elem}
			<button type="button" on:click={() => changeValue(elem)}>{elem}</button>
		{/each}

		<label>
			Введите свой цвет
			<input type="text" bind:value />
		</label>

		<p>{value}</p>
		<button
			type="button"
			on:click={() => {
				choiceColorFur(value);
				closeColorFurModal();
			}}>Подтвердить цвет шёрстки</button
		>
	</Modal>
{/if}

<style></style>
