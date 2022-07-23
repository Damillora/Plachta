<script lang="ts">
</script>

<li class="nav-menu">
	<slot></slot>
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

		a {
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
			a {
				color: var(--highlight-color);
			}
		}
		&.selected {
			background-color: var(--primary-color);
			display: flex;
			a {
				color: var(--primary-bg-color);
			}
		}
	}
</style>
