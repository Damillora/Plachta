<script lang="ts">
	interface Props {
		children?: import('svelte').Snippet;
	}

	let { children }: Props = $props();
</script>

<div class="card__description">
	{@render children?.()}
</div>

<style lang="scss">
	@import '../../styles/global';

	.card__description {
		margin-top: 0rem;
		margin-bottom: 0.5rem;

		flex-grow: 1;
	}
</style>
