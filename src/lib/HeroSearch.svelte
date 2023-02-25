<script lang="ts">
	export let value: string;
	export let fn: any;
</script>

<div class="hero">
	<img src="/backgroundImg.png" alt="">
	<div class="searchBar">
		<span class="material-symbols-rounded">
			work
		</span>
		<input bind:value={value} type="text" placeholder="Title, companies, expertise or benefits" />
		<button on:click={fn}>Search</button>
	</div>
</div>

<style>
	.hero {
		max-width: 1200px;
		margin: 0 12px;
		position: relative;
		padding-bottom: 42px;
		user-select: none;
	}

	.hero img {
		width: 100%;
		height: 138px;
		object-fit: cover;
		border-radius: 8px;
	}

	.searchBar {
		position: absolute;
		top: calc(50% - 21px);
		left: 50%;
		transform: translate(-50%, -50%);
		width: calc(790px - 8px);
		height: calc(55px - 8px);
		padding: 4px;
		display: flex;
		justify-content: space-between;
		align-items: center;
		background: #FFFFFF;
		box-shadow: 0px 2px 8px rgba(0, 0, 0, 0.1);
		border-radius: 4px;
		gap: 10px;
		font-family: 'Roboto';
		font-style: normal;
	}

	.searchBar input {
		width: 100%;
		border: none;
		outline: none;
		color: #282538;
		font-weight: 400;
		font-size: 12px;
		line-height: 14px;
	}

	.searchBar span {
		width: 24px;
		height: 24px;
		margin-left: 10px;
	}

	.searchBar span, .searchBar input::placeholder {
		color: #B9BDCF;
	}

	.searchBar button {
		background: #1E86FF;
		border-radius: 4px;
		width: 146px;
		height: 47px;
		border: none;
		cursor: pointer;
		font-weight: 500;
		font-size: 16px;
		line-height: 19px;
		color: #FFFFFF;
	}

	@media screen and (max-width: 826px) {
		.searchBar {
			left: 0;
			top: calc(50% - 21px);
			transform: translate(0, -50%);
			width: calc(100% - 48px);
			margin: 0 18px;
		}
	}
</style>
