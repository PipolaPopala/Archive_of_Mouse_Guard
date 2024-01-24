<script>
	export let choiceNature;
	let value = 3;
	function changeUp() {
		value = value + 1;
	}
	function choiceTraitOne() {}
	function choiceTraitTwo() {}
</script>

<p>Мышиная природа</p>

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
<button type="button" on:click={() => choiceNature(value)}>Подтвердить значение природы</button>

<style></style>
