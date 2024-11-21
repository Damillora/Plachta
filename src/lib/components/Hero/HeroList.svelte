<script lang="ts">
	interface Props {
		children?: import('svelte').Snippet;
	}

	let { children }: Props = $props();
</script>

<div class="hero-list">
	{@render children?.()}
</div>

<style lang="scss">
	@import '../../styles/global';

	.hero-list {
		display: flex;
		flex-direction: row;
		flex-wrap: wrap;
	}
</style>
