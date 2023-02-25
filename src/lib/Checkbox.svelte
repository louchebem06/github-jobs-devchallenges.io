<script lang="ts">
	export let checked: boolean;
	export let label: string;
	export let onchange: any;
</script>

<div class="checkbox">
	<input on:change={onchange} id="label-{label}" type="checkbox" bind:checked={checked} />
	<label for="label-{label}">{label}</label>
</div>

<style>
	.checkbox {
		display: flex;
		gap: 12px;
		align-items: center;
		cursor: pointer;
		margin-left: 12px;
		margin-bottom: 33px;
		user-select: none;
	}

	label {
		font-family: 'Poppins';
		font-style: normal;
		font-weight: 500;
		font-size: 14px;
		line-height: 21px;
		color: #334680;
		cursor: pointer;
	}

	input {
		width: 18px;
		height: 18px;
		cursor: pointer;
	}
</style>
