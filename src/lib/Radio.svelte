<script lang="ts">
	export let name: string;
	export let value: string;
	export let checked: boolean = false;
	export let group: string;
	export let onchange: any;
	export let search: string;
</script>

<div class="radio">
	<input on:change={() => {search = "", onchange()}} bind:group={group} id="{name}-{value}" type="radio" {name} {value} {checked} />
	<label for="{name}-{value}">{value}</label>
</div>

<style>
	.radio {
		display: flex;
		align-items: center;
		gap: 12.5px;
		cursor: pointer;
		user-select: none;
		margin-left: 12px;
	}

	input {
		-webkit-appearance: none;
		width: 18px;
		height: 18px;
		border-radius: 59px;
		outline: none;
		box-shadow: 0 0 0 2px #B9BDCF;
		position: relative;
		cursor: pointer;
	}

	input:checked {
		box-shadow: 0 0 0 2px #1E86FF;
	}

	input:before {
		content: '';
		display: block;
		width: 12px;
		height: 12px;
		border-radius: 50%;
		position: absolute;
		top: 50%;
		left: 50%;
		transform: translate(-50%, -50%);
	}

	input:checked:before {
		background: #1E86FF;
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
</style>
