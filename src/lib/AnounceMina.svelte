<script lang="ts">
  	import Image from "$lib/Image.svelte";
	import TextLogo from "$lib/TextLogo.svelte";

	export let fulltime: boolean = false;
	export let img: string;
	export let company: string;
	export let title: string;
	export let day: number;
	export let city: string;

	let text: string = `${day} day`;
	text += (day > 1) ? "s ago" : " ago";
</script>

<div class="anounce">
	<Image src={img} />
	<div class="content">
		<h1>{company}</h1>
		<h2>{title}</h2>
		<div class="endLine">
			{#if fulltime}
				<p class="fulltime">Full time</p>
			{/if}
			<div class="textLogos">
				<TextLogo logo="public" text={city} />
				<TextLogo logo="access_time" {text} />
			</div>
		</div>
	</div>
</div>

<style>
	.content {
		display: flex;
		flex-direction: column;
		justify-content: space-between;
		width: 100%;
	}

	.endLine {
		display: flex;
	}

	.textLogos {
		display: flex;
		gap: 28.5px;
		width: 100%;
		justify-content: flex-end;
		margin-right: 12px;
	}

	.anounce {
		width: 100%;
		height: calc(114px - 24px);
		background: #FFFFFF;
		box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.05);
		border-radius: 4px;
		margin-bottom: 32px;
		font-family: 'Roboto';
		font-style: normal;
		color: #334680;
		display: flex;
		gap: 16px;
		padding: 12px 0;
		cursor: pointer;
	}

	.anounce p.fulltime {
		width: 63px;
		height: 26px;
		border: 1px solid #334680;
		border-radius: 4px;
		text-align: center;
		line-height: 26px;
		font-weight: 700;
		font-size: 12px;
	}

	.anounce h1 {
		font-weight: 700;
		font-size: 12px;
		line-height: 14px;
	}

	.anounce h2 {
		font-weight: 400;
		font-size: 18px;
		line-height: 21px;
	}

	@media screen and (max-width: 866px) {
		.endLine {
			flex-direction: column;
			gap: 30px
		}

		.textLogos {
			justify-content: flex-start;
		}
		.anounce {
			width: 100%;
			height: calc(147px - 24px);
		}
	}
</style>
