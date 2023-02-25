<script lang="ts">
	import Checkbox from "$lib/Checkbox.svelte";
	import Radio from "$lib/Radio.svelte";
	import OptionSearch from "$lib/OptionSearch.svelte";

	export let checked: boolean;
	export let option: string;
	export let onchange: any;
	export let value: string;
</script>

<Checkbox onchange={onchange} bind:checked={checked} label="Full time"/>

<h3>Location</h3>

<OptionSearch onchange={onchange} bind:option={option} bind:value={value}/>

<div class="radios">
	<Radio onchange={onchange} bind:group={option} name="city" value="London" bind:search={value} />
	<Radio onchange={onchange} bind:group={option} name="city" value="Amsterdam" bind:search={value} />
	<Radio onchange={onchange} bind:group={option} name="city" value="New York" bind:search={value} />
	<Radio onchange={onchange} bind:group={option} name="city" value="Berlin" bind:search={value} />
</div>

<style>
	h3 {
		font-family: 'Poppins';
		font-style: normal;
		font-weight: 700;
		font-size: 14px;
		line-height: 21px;
		text-transform: uppercase;
		color: #B9BDCF;
		user-select: none;
	}

	.radios {
		display: flex;
		flex-direction: column;
		gap: 21px;
	}
</style>
