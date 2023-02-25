<script lang="ts">
	export let icon: string | undefined = undefined;
	export let border: boolean = false;
	export let value: number | undefined = undefined;
	export let clicked: boolean = false;
	export let not: boolean = false;
</script>

<div
	class="button"
	class:border={border}
	class:clicked={clicked}
	class:not={not}>
	{#if icon != undefined}
	<span class="material-symbols-rounded">
		{icon}
	</span>
	{/if}
	{#if value != undefined}
		<p>{value}</p>
	{/if}
</div>

<style>
	.button {
		width: 36px;
		height: 36px;
		border-radius: 4px;
		color: #B7BCCE;
		display: flex;
		align-items: center;
		justify-content: center;
		font-family: 'Roboto';
		font-style: normal;
		font-weight: 400;
		font-size: 12px;
		line-height: 14px;
	}

	.button:hover {
		color: #1E86FF;
	}

	.border:hover {
		border: 1px solid #1E86FF;
	}

	.clicked {
		background: #1E86FF;
		border: 1px solid #1E86FF!important;
		border-radius: 4px;
		color: #FFFFFF!important;
		cursor: default!important;
	}

	.border {
		border: 1px solid #B7BCCE;
		border-radius: 4px;
		cursor: pointer;
	}

	.not:hover {
		color: #B7BCCE!important;
		cursor: default!important;
	}
</style>
