<script lang="ts">
	interface Props {
		loading?: boolean;
	}

	let { loading = true }: Props = $props();
</script>

<div class="navigation-loading" class:navigation-loading--loading={loading}>
	<div class="navigation-loading__background"></div>
	<div class="navigation-loading__loading">
		<div class="navigation-loading__loading-icon"></div>
	</div>
</div>

<style lang="scss">
	@use '../../styles/global' as *;
	.navigation-loading {
		display: none;
		position: fixed;
		top: 0;
		left: 0;

		&--loading {
			display: flex;
		}

		&__background {
			background-color: var(--primary-bg-color);
			opacity: 0.5;
			position: fixed;
			top: 0;
			left: 0;
			width: 100vw;
			height: 100vh;
		}
		&__loading {
			position: fixed;
			bottom: calc(50vh - 2rem);
			left: calc(50vw - 2rem);
			width: 4rem;
			height: 4rem;
			display: flex;
			justify-content: center;
			align-items: center;
		}
		&__loading-icon {
			width: 4rem;
			aspect-ratio: 1;
			border-radius: 50%;
			border: 0.5rem solid var(--highlight-bg-color);
			border-right-color: var(--highlight-color);
			animation: l2 1s infinite linear;
		}
		@keyframes l2 {to{transform: rotate(1turn)}}
	}
</style>
