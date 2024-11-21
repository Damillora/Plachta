<script lang="ts">
	import type { Snippet } from 'svelte';
	
	interface Props {
		children?: Snippet;
	}

	let { children }: Props = $props();
</script>

<div class="page-header-contents">
	{@render children?.()}
</div>

<style lang="scss">
	@use '../../styles/global' as *;

	.page-header-contents {
		@include py(1rem);
		@include px(1rem);
	}
</style>
