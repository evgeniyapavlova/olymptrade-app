<script>
	export let isFirstActive, buttonLabels;
</script>

<div class="switch-buttons">
	<button
		class={isFirstActive ? 'is-active' : 'non-active'}
		on:click={() => {
			isFirstActive = true;
		}}>{buttonLabels.left}</button
	>
	<button
		class={!isFirstActive ? 'is-active' : 'non-active'}
		on:click={() => {
			isFirstActive = false;
		}}>{buttonLabels.right}</button
	>
</div>

<style>
	.switch-buttons {
		border-bottom: 1px solid rgba(255, 255, 255, 0.6);
		display: flex;
		align-items: flex-end;
		justify-content: flex-start;
	}

	.switch-buttons button {
		border: 1px solid rgba(255, 255, 255, 0.6);
		display: block;
		padding: 10px 20px;
		border-radius: 8px 8px 0 0;
		border-bottom: 1px solid transparent;
		margin-bottom: -1px;
		margin-right: 6px;
		cursor: pointer;
		/* transition: border 0.2s ease-out; */
		transition: background-color 0.2s ease-out;
		background-color: rgba(255, 255, 255, 0.1);
	}
	.switch-buttons button.is-active {
		border-bottom: 1px solid var(--dark-bgr);
		background-color: transparent;
	}
</style>
