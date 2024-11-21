<script lang="ts">
	interface Props {
		children?: import('svelte').Snippet;
	}

	let { children }: Props = $props();
</script>

<div class="page-header-contents">
	{@render children?.()}
</div>

<style lang="scss">
	@import '../../styles/global';

	.page-header-contents {
		@include py(1rem);
		@include px(1rem);
	}
</style>
