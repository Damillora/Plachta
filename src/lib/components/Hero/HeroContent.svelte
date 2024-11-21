<script lang="ts">
	import Container from '../Container/Container.svelte';
	import Post from '../PageTypes/Post.svelte';
	interface Props {
		children?: import('svelte').Snippet;
	}

	let { children }: Props = $props();
</script>

<div class="hero-content">
	<Container>
		<Post>
			{@render children?.()}
		</Post>
	</Container>
</div>

<style lang="scss">
	@import '../../styles/global';

	.hero-content {
		position: absolute;
		background-color: rgba(0, 0, 0, 0.5);
		color: $text-dark;
		left: 0;
		right: 0;
		top: 0;
		bottom: 0;

		:global(p),
		:global(h1),
		:global(h2),
		:global(h3),
		:global(h4),
		:global(h5),
		:global(h6),
		:global(a) {
			color: $text-dark;
		}

		&--light {
			background-color: rgba(255, 255, 255, 0.5);
			color: $text-light;

			:global(p),
			:global(h1),
			:global(h2),
			:global(h3),
			:global(h4),
			:global(h5),
			:global(h6),
			:global(a) {
				color: $text-light;
			}
		}
	}
</style>
