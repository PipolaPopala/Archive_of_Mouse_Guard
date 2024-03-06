<script>
	import Modal from '../Modal.svelte';
	export let rank;
	let showRank = false;
	function openRankModal() {
		showRank = true;
	}
	function closeRankModal() {
		showRank = false;
	}
	let value = '';
	function changeValue(elem) {
		value = elem;
	}
	function choiceRank(value) {
		rank = value;
	}
</script>

<button on:click={openRankModal}> {rank || 'Выберите ранг персонажа'} </button>
{#if showRank}
	<Modal close={closeRankModal} title="Выберите ранг персонажа">
		<p>
			(здесь можно расположить рисунки 5-х мышей соответствующего ранга, над ними название ранга,
			под ними описание, очень наглядно и красивенько. При нажатии внизу появляется вся инфа про
			этот ранг, и кнопка для подтверждения этого ранга)
		</p>

		<button type="button" on:click={() => changeValue('Лапа помощи')}>Лапа помощи</button>
		<button type="button" on:click={() => changeValue('Страж')}>Страж</button>
		<button type="button" on:click={() => changeValue('Патрульный')}>Патрульный</button>
		<button type="button" on:click={() => changeValue('Лидер патруля')}>Лидер патруля</button>
		<button type="button" on:click={() => changeValue('Капитан')}>Капитан</button>

		<p>{value}</p>
		<button
			type="button"
			on:click={() => {
				choiceRank(value);
				closeRankModal();
			}}>Подтвердить выбор ранга</button
		>
	</Modal>
{/if}

<style></style>
