<script lang="ts">
	import type { Snippet } from 'svelte';
	
	interface Props {
		children?: Snippet;
	}

	let { children }: Props = $props();
</script>

<h2 class="card__title">
	{@render children?.()}
</h2>

<style lang="scss">
	@use '../../styles/global' as *;

	.card__title {
		margin-top: 0;
		margin-bottom: 0.5rem;
		font-size: $text-2xl;
	}
</style>
