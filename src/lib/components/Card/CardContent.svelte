<script lang="ts">
	import type { Snippet } from 'svelte';
	
	interface Props {
		children?: Snippet;
	}

	let { children }: Props = $props();
</script>

<div class="card__content">
	{@render children?.()}
</div>

<style lang="scss">
	@use '../../styles/global' as *;

	.card__content {
		@include mx(1rem);
		@include my(1rem);

        display: flex;
        flex-direction: column;
        
		& > :global(*) {
			margin-top: 0rem;
			margin-bottom: 0.5rem;
		}
	}
</style>
