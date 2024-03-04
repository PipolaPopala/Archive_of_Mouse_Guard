<script>
	import Modal from '../Modal.svelte';
	export let nature;
	let showNature = false;
	function openNatureModal() {
		showNature = true;
	}
	function closeNatureModal() {
		showNature = false;
	}
	let value = 3;
	function changeUp() {
		value = value + 1;
	}
	function choiceTraitOne() {}
	function choiceTraitTwo() {}
	function choiceNature(value) {
		nature = value;
	}
</script>

<button on:click={openNatureModal}> Мышиная природа </button>
{#if showNature}
	<Modal close={closeNatureModal} title="Определите мышиную природу">
		<p>
			(занятно было бы нарисовать эти ситуации в виде комикса, с описанием того, на что повлияет
			каждый из выборов)
		</p>

		<p>
			Ваш персонаж готовится к зиме и ограничивает себя, или он использует то, что у него есть, как
			только потребуется?
		</p>
		<button type="button" on:click={changeUp}>Готовится к зиме</button>
		<button type="button" on:click={choiceTraitOne}>Использует всё при необходимости</button>

		<p>
			В конфликтных ситуациях ваш персонаж отстаивает свои решения и убеждения до конца, или может
			сбежать и где-нибудь отсидеться?
		</p>
		<button type="button" on:click={changeUp}>Может сбежать и отсидеться</button>
		<button type="button">Стоит до конца</button>

		<p>Ваш персонаж боится фиинов и сов, ласок и волков?</p>
		<button type="button" on:click={changeUp}>Боится за свою жизнь</button>
		<button type="button" on:click={choiceTraitTwo}>Боится, но борится с этим страхом</button>

		<p>{value}</p>
		<button
			type="button"
			on:click={() => {
				choiceNature(value);
				closeNatureModal();
			}}>Подтвердить значение природы</button
		>
	</Modal>
{/if}

<style></style>
