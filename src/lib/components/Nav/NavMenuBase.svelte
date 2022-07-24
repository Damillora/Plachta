<script lang="ts">
</script>

<li class="nav-menu">
	<slot />
</li>

<style lang="scss">
	@import '../../styles/global';

	.nav-menu {
		@include px(1.5rem);
		@include py(0.5rem);
		@include transition;
		background-color: var(--bg-color);
		border-radius: 1rem;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		color: var(--primary-color);
		cursor: pointer;

		:global(a) {
			&:hover,
			&:active,
			&:visited,
			&:focus {
				text-decoration: none;
			}
			color: var(--primary-color);
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
	}
</style>
