<script lang="ts">
	import type { Snippet } from 'svelte';
	
	interface Props {
		children?: Snippet;
	}

	let { children }: Props = $props();
</script>

<div class="card__footer">
	{@render children?.()}
</div>

<style lang="scss">
	@use '../../styles/global' as *;

	.card__footer {
        margin-bottom: 0rem;
		display: flex;
		flex-direction: row;
		align-items: center;
	}
</style>
