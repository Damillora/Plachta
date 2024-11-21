<script lang="ts">
	import type { Snippet } from 'svelte';
	
	interface Props {
		children?: Snippet;
	}

	let { children }: Props = $props();
</script>

<div class="notice">
	{@render children?.()}
</div>

<style lang="scss">
	@use '../../styles/global' as *;

	.notice {
		background: var(--primary-bg-color);
		color: var(--primary-color);
		padding: 1.25rem;
		border: 1px solid var(--primary-color);
		margin-bottom: 1rem;
	}
</style>
