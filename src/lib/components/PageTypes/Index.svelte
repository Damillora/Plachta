<script lang="ts">
	import type { Snippet } from 'svelte';
	
	interface Props {
		children?: Snippet;
	}

	let { children }: Props = $props();
</script>

<main class="index">
	{@render children?.()}
</main>

<style lang="scss">
	@use '../../styles/global' as *;
	.index {
		@include my(2rem);
		@include px(1rem);
	}
</style>
