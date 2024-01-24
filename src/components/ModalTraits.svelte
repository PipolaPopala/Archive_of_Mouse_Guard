<script>
	export let choiceExperience;
	let value = [];
	function changeValue(elem) {
		value = [...value, elem];
	}
	let traitBirth = [
		{ title: 'Бдительный', description: '' },
		{ title: 'Безрассудный', description: '' },
		{ title: 'Бестрашный', description: '' },
		{ title: 'Большелапый', description: '' },
		{ title: 'Боязливый', description: '' },
		{ title: 'Вдумчивый', description: '' },
		{ title: 'Волчий нюх', description: '' },
		{ title: 'Высокий', description: '' },
		{ title: 'Грациозный', description: '' },
		{ title: 'Длиннохвостый', description: '' },
		{ title: 'Доверие Стражи', description: '' },
		{ title: 'Дотошный', description: '' },
		{ title: 'Жаворонок', description: '' },
		{ title: 'Защитник', description: '' },
		{ title: 'Золотые лапы', description: '' },
		{ title: 'Зоркий', description: '' },
		{ title: 'Крепкий', description: '' },
		{ title: 'Лидер', description: '' },
		{ title: 'Любопытный', description: '' },
		{ title: 'Мелкий', description: '' },
		{ title: 'Метеочувствительный', description: '' },
		{ title: 'Мудрый', description: '' },
		{ title: 'Невинный', description: '' },
		{ title: 'Недоверчивый', description: '' },
		{ title: 'Независимый', description: '' },
		{ title: 'Непреклонный', description: '' },
		{ title: 'Острозубый', description: '' },
		{ title: 'Острый слух', description: '' },
		{ title: 'Отзывчивый', description: '' },
		{ title: 'Открытый', description: '' },
		{ title: 'Пессимист', description: '' },
		{ title: 'Покрытый шрамами', description: '' },
		{ title: 'Проворный', description: '' },
		{ title: 'Путешественник', description: '' },
		{ title: 'Пылкий', description: '' },
		{ title: 'Рациональный', description: '' },
		{ title: 'Решительный', description: '' },
		{ title: 'Седошкурый', description: '' },
		{ title: 'Скептичный', description: '' },
		{ title: 'Сова', description: '' },
		{ title: 'Сообразительный', description: '' },
		{ title: 'Спокойный', description: '' },
		{ title: 'Стойкий', description: '' },
		{ title: 'Телохранитель', description: '' },
		{ title: 'Тихий', description: '' },
		{ title: 'Толстый', description: '' },
		{ title: 'Топографический кретин', description: '' },
		{ title: 'Тощий', description: '' },
		{ title: 'Трудолюбивый', description: '' },
		{ title: 'Умный', description: '' },
		{ title: 'Упрямый', description: '' },
		{ title: 'Хитрый', description: '' },
		{ title: 'Храбрый', description: '' },
		{ title: 'Чёрствый', description: '' },
		{ title: 'Щедрый', description: '' },
		{ title: 'Экстраверт', description: '' },
		{ title: 'Юный', description: '' }
	];
	let traitParents = [
		{ title: 'Бестрашный', description: '' },
		{ title: 'Большелапый', description: '' },
		{ title: 'Боязливый', description: '' },
		{ title: 'Волчий нюх', description: '' },
		{ title: 'Высокий', description: '' },
		{ title: 'Грациозный', description: '' },
		{ title: 'Длиннохвостый', description: '' },
		{ title: 'Жаворонок', description: '' },
		{ title: 'Защитник', description: '' },
		{ title: 'Крепкий', description: '' },
		{ title: 'Любопытный', description: '' },
		{ title: 'Мелкий', description: '' },
		{ title: 'Недоверчивый', description: '' },
		{ title: 'Независимый', description: '' },
		{ title: 'Острозубый', description: '' },
		{ title: 'Острый слух', description: '' },
		{ title: 'Отзывчивый', description: '' },
		{ title: 'Открытый', description: '' },
		{ title: 'Покрытый шрамами', description: '' },
		{ title: 'Проворный', description: '' },
		{ title: 'Путешественник', description: '' },
		{ title: 'Пылкий', description: '' },
		{ title: 'Решительный', description: '' },
		{ title: 'Скептичный', description: '' },
		{ title: 'Сообразительный', description: '' },
		{ title: 'Спокойный', description: '' },
		{ title: 'Тихий', description: '' },
		{ title: 'Топографический кретин', description: '' },
		{ title: 'Тощий', description: '' },
		{ title: 'Трудолюбивый', description: '' },
		{ title: 'Умный', description: '' },
		{ title: 'Упрямый', description: '' },
		{ title: 'Храбрый', description: '' },
		{ title: 'Щедрый', description: '' },
		{ title: 'Экстраверт', description: '' }
	];
	let traitLife = [
		{ title: 'Бдительный', description: '' },
		{ title: 'Бестрашный', description: '' },
		{ title: 'Боязливый', description: '' },
		{ title: 'Вдумчивый', description: '' },
		{ title: 'Дотошный', description: '' },
		{ title: 'Жаворонок', description: '' },
		{ title: 'Защитник', description: '' },
		{ title: 'Золотые лапы', description: '' },
		{ title: 'Зоркий', description: '' },
		{ title: 'Крепкий', description: '' },
		{ title: 'Лидер', description: '' },
		{ title: 'Любопытный', description: '' },
		{ title: 'Метеочувствительный', description: '' },
		{ title: 'Мудрый', description: '' },
		{ title: 'Непреклонный', description: '' },
		{ title: 'Отзывчивый', description: '' },
		{ title: 'Пессимист', description: '' },
		{ title: 'Покрытый шрамами', description: '' },
		{ title: 'Путешественник', description: '' },
		{ title: 'Рациональный', description: '' },
		{ title: 'Седошкурый', description: '' },
		{ title: 'Скептичный', description: '' },
		{ title: 'Сова', description: '' },
		{ title: 'Спокойный', description: '' },
		{ title: 'Стойкий', description: '' },
		{ title: 'Телохранитель', description: '' },
		{ title: 'Тихий', description: '' },
		{ title: 'Тощий', description: '' },
		{ title: 'Умный', description: '' },
		{ title: 'Хитрый', description: '' },
		{ title: 'Храбрый', description: '' },
		{ title: 'Чёрствый', description: '' }
	];
</script>

<p>С какой чертой родился ваш персонаж?</p>
{#each traitBirth as { title, description }}
	<button type="button" on:click={() => changeValue(title)} title={description}>
		{title}
	</button>
{/each}

<p>Какую черту пероснаж унаследовал от родителей?</p>
{#each traitParents as { title, description }}
	<button type="button" on:click={() => changeValue(title)} title={description}>
		{title}
	</button>
{/each}

<p>Жизнь в пути</p>
{#each traitLife as { title, description }}
	<button type="button" on:click={() => changeValue(title)} title={description}>
		{title}
	</button>
{/each}

<p>{value}</p>
<button type="button" on:click={() => choiceExperience(value)}>Подтвердить выбор черт</button>

<style></style>
