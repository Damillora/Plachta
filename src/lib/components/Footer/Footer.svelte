<script lang="ts">
	import type { Snippet } from 'svelte';
	
	interface Props {
		children?: Snippet;
	}

	let { children }: Props = $props();
</script>

<footer class="footer">
	{@render children?.()}
</footer>

<style lang="scss">
	@use '../../styles/global' as *;

	.footer {
		min-height: 3rem;
		background-color: var(--primary-color);
		color: var(--primary-bg-color);
		display: flex;
		align-items: center;
		@include px(1rem);
		@include py(1rem);
		:global(p) {
			margin: 0;
		}
	}
</style>
