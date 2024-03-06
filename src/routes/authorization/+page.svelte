<script>
	let register = false;
	let email = '';
	let password = '';
	let confirmPassword = '';
	async function handleSubmit() {
	}
</script>

<svelte:head>
	<title>Authorization</title>
	<meta name="description" content="Authorization" />
</svelte:head>

<section>
	<h1>{register ? 'Регистрация' : 'Авторизация'}</h1>
	<form>
		<label>
			<input bind:value={email} type="email" placeholder="Email" />
		</label>
		<label>
			<input bind:value={password} type="password" placeholder="Password" />
		</label>
		{#if register}
			<label>
				<input bind:value={confirmPassword} type="password" placeholder="Confirm password" />
			</label>
		{/if}
		<button on:click={handleSubmit}>Войти</button>
	</form>
	<div class="change-form">
		{#if register}
			<p>У вас уже есть аккаунт?</p>
			<button on:click={() => (register = false)}>Войти</button>
		{:else}
			<p>У вас не аккаунта?</p>
			<button on:click={() => (register = true)}>Зарегистрироваться</button>
		{/if}
		<button on:click={() => authHandlers.resetPassword(email)}>Забыли пароль?</button>
	</div>
</section>

<style>
	section {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		row-gap: 20px;
	}
	form {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		row-gap: 10px;
	}
	.change-form {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
	}
</style>
