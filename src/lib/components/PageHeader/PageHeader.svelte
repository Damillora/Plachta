<script lang="ts">
	import type { Snippet } from 'svelte';
	
	interface Props {
		children?: Snippet;
	}

	let { children }: Props = $props();
</script>

<div class="page-header">
	{@render children?.()}
</div>

<style lang="scss">
	@use '../../styles/global' as *;

	.page-header {
		background-color: var(--primary-color);
		color: var(--primary-bg-color);
		border-radius: 20px;
		margin-bottom: 1rem;
		margin-top: 1rem;
		@include mx(0.5rem);
		@include shadow;

		:global(h1),
		:global(h2),
		:global(h3),
		:global(h4),
		:global(h5),
		:global(h6),
		:global(a),
		:global(p) {
			color: var(--primary-bg-color);
		}
	}
</style>
