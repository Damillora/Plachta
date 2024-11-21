<script lang="ts">
	import type { Snippet } from 'svelte';
	
	interface Props {
		shown?: boolean;
		children?: Snippet;
	}

	let { shown = false, children }: Props = $props();
</script>

<nav class="nav" class:nav--shown={shown}>
	{@render children?.()}
</nav>

<style lang="scss">
	@use '../../styles/global' as *;
	.nav {
		list-style-type: none;
		display: none;
		flex-direction: column;
		text-align: center;

		@include screen(md) {
			display: flex;
			flex-direction: row;
		}

		&--shown {
			display: flex;
			flex-direction: column;
		}
	}
</style>
