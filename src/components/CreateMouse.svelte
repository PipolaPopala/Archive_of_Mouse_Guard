<script>
	import Name from './name/Name.svelte';
	import Rank from './rank/Rank.svelte';
  import Home from './home/Home.svelte';
  import Skills from './skills/Skills.svelte';
  import Nature from './nature/Nature.svelte';
  import Knowledge from './knowledge/Knowledge.svelte';
  import Traits from './traits/Traits.svelte';
  import ColorFur from './colorFur/ColorFur.svelte';
  import ColorCloak from './colorCloak/ColorCloak.svelte';

	let concept = '';

	let age = 0;

	let name = '';
	function choiceName(value) {
		name = value;
	}

	let rank = '';
	function choiceRank(value) {
		rank = value;
	}

	let home = {};
	function choiceHome(value) {
		home = value;
	}

	let skills = [];
	function choiceSkills(value) {
		skills = value;
	}

	let nature = 3;
	function choiceNature(value) {
		nature = value;
	}

	let knowledge = [];
	function choiceKnowledge(value) {
		knowledge = value;
	}

	let traits = [];
	function choiceTraits(value) {
		traits = value;
	}

	let colorFur = '';
	function choiceColorFur(value) {
		colorFur = value;
	}

	let colorCloak = '';
	function choiceColorCloak(value) {
		colorCloak = value;
	}

	let parents = [];
	let master = '';
	let mentor = '';
	let friend = '';
	let enemy = '';
	let belief = '';
	let instinct = '';
	let goal = '';
	let equipment = '';
</script>

<label>
	<p>Концепция персонажа</p>
	<textarea name="" cols="30" rows="3" bind:value={concept}></textarea>
</label>
<p>{concept}</p>

<Name {choiceName} />
<p>{name}</p>

<Rank {choiceRank} />
<p>{rank}</p>

<Home {choiceHome} />
<p>{home.name}</p>

<Skills {choiceSkills} />
<p>{skills}</p>

<Nature {choiceNature} />
<p>{nature}</p>

<Knowledge {choiceKnowledge} />
<p>{knowledge}</p>

<Traits {choiceTraits} />
<p>{traits}</p>

<ColorFur {choiceColorFur} />
<p>{colorFur}</p>

<ColorCloak {choiceColorCloak} />
<p>{colorCloak}</p>

<label>
	<p>Назовите родителей</p>
	<textarea name="" cols="30" rows="3" bind:value={parents}></textarea>
</label>
<p>{parents}</p>

<label>
	<p>Назовите мастера</p>
	<textarea name="" cols="30" rows="3" bind:value={master}></textarea>
</label>
<p>{master}</p>

<label>
	<p>Назовите наставника</p>
	<textarea name="" cols="30" rows="3" bind:value={mentor}></textarea>
</label>
<p>{mentor}</p>

<label>
	<p>Назовите друга</p>
	<textarea name="" cols="30" rows="3" bind:value={friend}></textarea>
</label>
<p>{friend}</p>

<label>
	<p>Назовите врага</p>
	<textarea name="" cols="30" rows="3" bind:value={enemy}></textarea>
</label>
<p>{enemy}</p>

<label>
	<p>Убеждение</p>
	<textarea name="" cols="30" rows="3" bind:value={belief}></textarea>
</label>
<p>{belief}</p>

<label>
	<p>Инстинкты</p>
	<textarea name="" cols="30" rows="3" bind:value={instinct}></textarea>
</label>
<p>{instinct}</p>

<label>
	<p>Цели</p>
	<textarea name="" cols="30" rows="3" bind:value={goal}></textarea>
</label>
<p>{goal}</p>

<label>
	<p>Снаряжение</p>
	<textarea name="" cols="30" rows="3" bind:value={equipment}></textarea>
</label>
<p>{equipment}</p>

<p>Где-то разместить проверочные баллы, баллы судьбы и баллы личности</p>

<style>
</style>
