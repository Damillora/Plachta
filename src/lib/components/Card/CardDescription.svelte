<script lang="ts">
	import type { Snippet } from 'svelte';
	
	interface Props {
		children?: Snippet;
	}

	let { children }: Props = $props();
</script>

<div class="card__description">
	{@render children?.()}
</div>

<style lang="scss">
	@use '../../styles/global' as *;

	.card__description {
		margin-top: 0rem;
		margin-bottom: 0.5rem;

		flex-grow: 1;
	}
</style>
