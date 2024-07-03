<script>
	import { slide } from 'svelte/transition';
	export let item;
	export let open = false;

	const { question, text } = item;
	const handleClick = () => (open = !open);
</script>

<div class="accordion-item">
	<button class="item-label" on:click={handleClick}>
		<button class="{open ? 'item-open' : 'item-closed'} arrow"></button>
		<div class="question">
			{question}
		</div>
	</button>

	{#if open}
		<div class="answer" transition:slide>{text}</div>
	{/if}
</div>

<style>
	.question {
		font-weight: 600;
	}
	.item-label {
		display: flex;
		align-items: center;
		justify-content: flex-start;
		cursor: pointer;
		gap: 15px;
	}
	.answer {
		margin-top: 20px;
	}
	.accordion-item {
		margin-bottom: 40px;
	}
	.arrow {
		width: 30px;
		height: 30px;
	}

	.arrow:after {
		content: '';
		display: block;
		border-right: solid var(--btn-blue);
		border-top: solid var(--btn-blue);
		width: 15px;
		height: 15px;
		transform: rotate(45deg);
		transform-origin: 50% 50%;
		transition: all ease-out 0.2s;
	}

	.arrow.item-open::after {
		transform: translate(4px, 6px) rotate(0);
		border-right: none;
	}

	@media screen and (max-width: 768px) {
		.item-label {
			font-size: 16px;
		}
		.answer {
			font-size: 14px;
		}
	}
</style>
