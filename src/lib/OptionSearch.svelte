<script lang="ts">
	export let onchange: any;
	export let value: string;
</script>

<div class="search">
	<span class="material-symbols-rounded">
		public
	</span>
	<input on:keydown={onchange} bind:value={value} type="text" placeholder="City, state, zip code or country"/>
</div>

<style>
	.search {
		width: 379px;
		height: calc(48px - 14px);
		left: 120px;
		top: 368px;
		background: #FFFFFF;
		box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.05);
		border-radius: 4px;
		margin-top: 14px;
		margin-bottom: 24px;
		padding: 14px;
		display: flex;
		align-items: center;
		color: #B9BDCF;
	}

	input {
		width: 100%;
		border: none;
		outline: none;
		color: #282538;
	}

	input::placeholder {
		color: #B9BDCF;
	}

	span {
		margin-right: 14px;
	}
</style>