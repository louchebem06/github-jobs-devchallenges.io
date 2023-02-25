<script lang="ts">
	export let logo: string;
	export let text: string;
</script>

<div class="textLogo">
	<span class="material-symbols-rounded">
		{logo}
	</span>
	<p>{text}</p>
</div>

<style>
	.textLogo {
		display: flex;
		align-items: center;
		font-family: 'Roboto';
		font-style: normal;
		font-weight: 500;
		font-size: 12px;
		line-height: 14px;
		color: #B7BCCE;
		gap: 7.5px;
	}
</style>
