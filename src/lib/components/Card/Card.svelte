<script lang="ts">
	interface Props {
		hasImage?: boolean;
		children?: import('svelte').Snippet;
	}

	let { hasImage = false, children }: Props = $props();
</script>

<div class="card" class:card--image={hasImage}>
	{@render children?.()}
</div>

<style lang="scss">
	@import '../../styles/global';

	.card {
		border-radius: 20px;
		@include shadow;
		margin-bottom: 2rem;
		display: flex;
		
		&--image {
			display: grid;
			grid-template-rows: 150px 1fr;
			grid-template-columns: 1fr;

			@include screen(md) {
				grid-template-rows: 1fr;
				grid-template-columns: 300px 6fr;
			}
		}
	}
</style>
