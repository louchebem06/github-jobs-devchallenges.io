<script lang="ts">
	export let name: string;
</script>

<header>
	<h1>{name}</h1>
	<h2>Jobs</h2>
</header>

<style>
	header {
		display: flex;
		gap: 5px;
		align-items: flex-end;
		font-family: 'Poppins';
		font-style: normal;
		color: #282538;
		font-size: 24px;
		line-height: 36px;
		max-width: 1200px;
		margin: auto 12px;
		padding: 32px 0;
		user-select: none;
	}

	header h1 {
		font-weight: 700;
	}

	header h2 {
		font-weight: 300;
	}
</style>
