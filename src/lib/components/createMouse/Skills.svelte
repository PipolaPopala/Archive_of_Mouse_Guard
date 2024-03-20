<script>
	import Modal from '../Modal.svelte';
	export let skills;
	let showSkills = false;
	function openSkillsModal() {
		showSkills = true;
	}
	function closeSkillsModal() {
		showSkills = false;
	}
	let value = [];
	function changeValue(elem) {
		value = [...value, elem];
	}
	function choiceSkills(value) {
		skills = value;
	}
	let skillsNature = [
		'Администратор',
		'Архивариус',
		'Боец',
		'Военный',
		'Гончар',
		'Знаток зверей',
		'Инструктор',
		'Каменщик',
		'Картограф',
		'Корабел',
		'Кузнец',
		'Лекарь',
		'Манипулятор',
		'Мельник',
		'Наблюдатель за погодой',
		'Насекомовод',
		'Оратор',
		'Оружейник',
		'Охотник',
		'Пекарь',
		'Переговорщик',
		'Пивовар',
		'Плотник',
		'Повар',
		'Пчеловод',
		'Разведчик',
		'Разнорабочий',
		'Сборщик',
		'Следопыт',
		'Специалист по выживанию',
		'Стекольщик',
		'Ткач',
		'Торгаш',
		'Учёный'
	];
	let skillsParents = [
		'Архивариус',
		'Гончар',
		'Каменщик',
		'Картограф',
		'Корабел',
		'Кузнец',
		'Мельник',
		'Насекомовод',
		'Оружейник',
		'Пекарь',
		'Пивовар',
		'Плотник',
		'Пчеловод',
		'Сборщик',
		'Стекольщик',
		'Ткач'
	];
	let skillsSocial = ['Манипулятор', 'Оратор', 'Переговорщик'];
	let skillsMaster = [
		'Архивариус',
		'Гончар',
		'Каменщик',
		'Картограф',
		'Кузнец',
		'Лекарь',
		'Мельник',
		'Насекомовод',
		'Оружейник',
		'Пекарь',
		'Пивовар',
		'Плотник',
		'Повар',
		'Пчеловод',
		'Разнорабочий',
		'Сборщик',
		'Стекольщик',
		'Ткач'
	];
	let skillsMentor = [
		'Боец',
		'Инструктор',
		'Лекарь',
		'Наблюдатель за погодой',
		'Охотник',
		'Разведчик',
		'Следопыт',
		'Специалист по выживанию'
	];
	let skillsSpecialization = [
		'Боец',
		'Инструктор',
		'Лекарь',
		'Наблюдатель за погодой',
		'Охотник',
		'Разведчик',
		'Следопыт',
		'Специалист по выживанию'
	];
</script>

<button on:click={openSkillsModal}> {skills.length < 1 ? 'Жизненный опыт персонажа' : skills} </button>
<p>Где-то здесь разместить навыки</p>
{#if showSkills}
	<Modal close={closeSkillsModal} title="Определите жизненный опыт персонажа">
		<p>
			(списки навыков, с описанием того, сколько навыков из каких списков можно выбрать. Может быть
			вставить картинки сответствующие вопросам, на которые следует ответить пероснажу, родителей,
			наставника и т.д.)
		</p>

		<p>В чём персонаж талантлив от природы?</p>
		{#each skillsNature as skill}
			<button type="button" on:click={() => changeValue(skill)}>
				{skill}
			</button>
		{/each}

		<p>Чему родители научили персонажа?</p>
		{#each skillsParents as skill}
			<button type="button" on:click={() => changeValue(skill)}>
				{skill}
			</button>
		{/each}

		<p>Как персонаж убеждает других сделать что-то или поверить ему?</p>
		{#each skillsSocial as skill}
			<button type="button" on:click={() => changeValue(skill)}>
				{skill}
			</button>
		{/each}

		<p>Какой мастер-ремесленник учил персонажа в Локхейвене?</p>
		{#each skillsMaster as skill}
			<button type="button" on:click={() => changeValue(skill)}>
				{skill}
			</button>
		{/each}

		<p>На что делал упор наставник-страж персонажа при обучении?</p>
		{#each skillsMentor as skill}
			<button type="button" on:click={() => changeValue(skill)}>
				{skill}
			</button>
		{/each}

		<p>На чём специализируется ваш персонаж?</p>
		{#each skillsSpecialization as skill}
			<button type="button" on:click={() => changeValue(skill)}>
				{skill}
			</button>
		{/each}

		<p>{value}</p>
		<button
			type="button"
			on:click={() => {
				choiceSkills(value);
				closeSkillsModal();
			}}>Подтвердить выбор черт</button
		>
	</Modal>
{/if}

<style></style>
