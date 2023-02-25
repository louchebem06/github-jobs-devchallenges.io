<script lang="ts">
	export let src: string;
	export let alt: string = "";
</script>

{#if src == undefined || src == ""}
	<div class="img">
	</div>
{:else}
	<img {src} {alt} />
{/if}

<style>
	.img, img {
		min-width: 90px;
		min-height: 90px;
		max-width: 90px;
		max-height: 90px;
		border-radius: 4px;
		object-fit: cover;
		margin-left: 12px;
	}

	.img {
		background-color: #F2F2F2;
		position: relative;
	}

	.img:before {
		position: absolute;
		content: "not found";
		top: 50%;
		left: 50%;
		transform: translate(-50%, -50%);
		font-family: 'Roboto';
		font-style: normal;
		font-weight: 500;
		font-size: 12px;
		line-height: 14px;
		color: #BDBDBD;
		white-space: nowrap;
	}
</style>