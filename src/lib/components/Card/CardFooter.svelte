<script lang="ts">
	interface Props {
		children?: import('svelte').Snippet;
	}

	let { children }: Props = $props();
</script>

<div class="card__footer">
	{@render children?.()}
</div>

<style lang="scss">
	@import '../../styles/global';

	.card__footer {
        margin-bottom: 0rem;
		display: flex;
		flex-direction: row;
		align-items: center;
	}
</style>
