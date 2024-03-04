<script>
	import Name from './Name.svelte';
	import Rank from './Rank.svelte';
  import Home from './Home.svelte';
  import Skills from './Skills.svelte';
  import Nature from './Nature.svelte';
  import Knowledge from './Knowledge.svelte';
  import Traits from './Traits.svelte';
  import ColorFur from './ColorFur.svelte';
  import ColorCloak from './ColorCloak.svelte';

	let concept = '';
	let age = 0;
	let name = '';
	let rank = '';
	let home = {};
	let skills = [];
	let nature = 3;
	let knowledge = [];
	let traits = [];
	let colorFur = '';
	let colorCloak = '';
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

<Name bind:name/>
<p>{name}</p>

<Rank bind:rank />
<p>{rank}</p>

<Home bind:home />
<p>{home.name}</p>

<Skills bind:skills />
<p>{skills}</p>

<Nature bind:nature />
<p>{nature}</p>

<Knowledge bind:knowledge />
<p>{knowledge}</p>

<Traits bind:traits />
<p>{traits}</p>

<ColorFur bind:colorFur />
<p>{colorFur}</p>

<ColorCloak bind:colorCloak />
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
