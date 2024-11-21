<script lang="ts">
	import type { Snippet } from 'svelte';
	
	interface Props {
		children?: Snippet;
	}

	let { children }: Props = $props();
</script>

<div class="hero-list">
	{@render children?.()}
</div>

<style lang="scss">
	@use '../../styles/global' as *;

	.hero-list {
		display: flex;
		flex-direction: row;
		flex-wrap: wrap;
	}
</style>
