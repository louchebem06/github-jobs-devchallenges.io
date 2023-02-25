<script lang="ts">
  import ButtonPagination from "./ButtonPagination.svelte";
</script>

<div class="buttons">
	<ButtonPagination icon="keyboard_arrow_left" border />
	<ButtonPagination value={1} border />
	<ButtonPagination value={2} border clicked/>
	<ButtonPagination value={3} border />
	<ButtonPagination icon="more_horiz" not/>
	<ButtonPagination value={10} border />
	<ButtonPagination icon="keyboard_arrow_right" border />
</div>

<style>
	.buttons {
		display: flex;
		gap: 12px;
		margin-bottom: 24px;
		justify-content: flex-end;
	}
</style>
