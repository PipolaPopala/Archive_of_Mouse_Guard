<script>
	import Modal from '../Modal.svelte';
	export let colorCloak;
	let showColorCloak = false;
	function openColorCloakModal() {
		showColorCloak = true;
	}
	function closeColorCloakModal() {
		showColorCloak = false;
	}
	let value = '';
	let colors = ['Коричневый', 'Русый', 'Серый', 'Чёрный', 'Белый', 'Рыжий'];
	function changeValue(elem) {
		value = elem;
	}
	function choiceColorCloak(value) {
		colorCloak = value;
	}
</script>

<button on:click={openColorCloakModal}> {colorCloak || 'Выберите цвет плаща'} </button>
{#if showColorCloak}
	<Modal close={closeColorCloakModal} title="Выберите цвет плаща">
		<p>
			(забавно было бы нарисовать некий эскиз мышки, или плаща, весящего на вешалке, и, при выборе
			цвета плащ меняется)
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
				choiceColorCloak(value);
				closeColorCloakModal();
			}}>Подтвердить цвет плаща</button
		>
	</Modal>
{/if}

<style></style>
