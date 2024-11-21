<script lang="ts">
	import type { Snippet } from 'svelte';
	
	interface Props {
		children?: Snippet;
	}

	let { children }: Props = $props();
</script>

<div class="container">
	{@render children?.()}
</div>

<style lang="scss">
	@use '../../styles/global' as *;
	.container {
		width: 100%;
		margin-left: auto;
		margin-right: auto;
		@include screen(sm) {
			max-width: 640px;
		}
		@include screen(md) {
			max-width: 768px;
		}
		@include screen(lg) {
			max-width: 1024px;
		}
		@include screen(xl) {
			max-width: 1280px;
		}
	}
</style>
