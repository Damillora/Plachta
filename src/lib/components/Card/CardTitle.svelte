<script lang="ts">
	interface Props {
		children?: import('svelte').Snippet;
	}

	let { children }: Props = $props();
</script>

<h2 class="card__title">
	{@render children?.()}
</h2>

<style lang="scss">
	@import '../../styles/global';

	.card__title {
		margin-top: 0;
		margin-bottom: 0.5rem;
		font-size: $text-2xl;
	}
</style>
