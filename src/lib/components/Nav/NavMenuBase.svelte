<script lang="ts">
	interface Props {
		children?: import('svelte').Snippet;
	}

	let { children }: Props = $props();
</script>

<li class="nav-menu">
	{@render children?.()}
</li>

<style lang="scss">
	@import '../../styles/global';

	.nav-menu {
		@include transition;
		background-color: var(--bg-color);
		border-radius: 1rem;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		color: var(--primary-color);
		cursor: pointer;

		@include screen(md) {
			margin-right: 0.75rem;
		}
		:global(a) {
			color: var(--primary-color);

			&:hover,
			&:active,
			&:visited,
			&:focus {
				text-decoration: none;
			}
		}
		&:hover {
			background-color: var(--highlight-bg-color);
			:global(a) {
				color: var(--highlight-color);
			}
		}
		&:global(.selected) {
			background-color: var(--primary-color);
			display: flex;
			:global(a) {
				color: var(--primary-bg-color);
			}
		}
		> :global(*) {
			@include px(1rem);
			@include py(0.5rem);
		}
	}
</style>
