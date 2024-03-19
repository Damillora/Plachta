<script lang="ts">
	import Container from '../Container/Container.svelte';
	import Post from '../PageTypes/Post.svelte';
</script>

<div class="hero-content">
	<Container>
		<Post>
			<slot />
		</Post>
	</Container>
</div>

<style lang="scss">
	@import '../../styles/global';

	.hero-content {
		position: absolute;
		background-color: rgba(0, 0, 0, 0.5);
		color: var(--bg-color);
		@include py(2rem);
		@include px(1rem);
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
		:global(h6) {
			color: var(--bg-color);
		}

		&--light {
			background-color: rgba(255, 255, 255, 0.5);
			color: var(--text-color);

			:global(p),
			:global(h1),
			:global(h2),
			:global(h3),
			:global(h4),
			:global(h5),
			:global(h6) {
				color: var(--text-color);
			}
		}
	}
</style>
