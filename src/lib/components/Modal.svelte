<script>
	export let close;
	export let title = 'Модальное окно';
</script>

<dialog>
	<div class="modal-header">
		<h2>{title}</h2>
		<button type="button" on:click={close}>х</button>
	</div>
	<div class="modal-content">
		<slot />
	</div>
</dialog>

<style>
	dialog {
		display: block;
		position: absolute;
		width: 60%;
		min-height: 40%;
		max-height: 80%;
		top: 10%;
		margin: 0 auto;
		z-index: 1000;
		background-color: #ffffff;
		padding: 20px;
		box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
		overflow-y: auto;
	}
	.modal-header {
		display: flex;
		align-items: center;
		justify-content: space-between;
	}
</style>
