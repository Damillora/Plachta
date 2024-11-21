<script lang="ts">
	import type { Snippet } from 'svelte';
	
	interface Props {
		children?: Snippet;
	}

	let { children }: Props = $props();
</script>

<main class="post">
	{@render children?.()}
</main>

<style lang="scss">
	@use '../../styles/global' as *;

	.post {
		@include my(2rem);
		@include px(1rem);
		@include mx(auto);

		@include screen(md) {
			max-width: 640px;
		}
		@include screen(lg) {
			max-width: 768px;
		}
	}
</style>
