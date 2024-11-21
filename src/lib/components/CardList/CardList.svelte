<script lang="ts">
	interface Props {
		children?: Snippet;
	}

	let { children }: Props = $props();
</script>

<div class="card-list">
	{@render children?.()}
</div>

<style lang="scss">
	.card-list {
		display: flex;
		flex-direction: column;
	}
</style>
