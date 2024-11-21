<script lang="ts">
	interface Props {
		children?: import('svelte').Snippet;
	}

	let { children }: Props = $props();
</script>

<main class="index">
	{@render children?.()}
</main>

<style lang="scss">
	@import '../../styles/global';
	.index {
		@include my(2rem);
		@include px(1rem);
	}
</style>
