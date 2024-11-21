<script lang="ts">
	interface Props {
		loading?: boolean;
	}

	let { loading = true }: Props = $props();
</script>

<div class="navigation-loading" class:navigation-loading--loading={loading}>
	<div class="navigation-loading__background"></div>
	<div class="navigation-loading__contents">
		<p>Loading</p>
	</div>
	<div class="navigation-loading__loading"></div>
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
		&__contents {
			color: var(--primary-color);
			position: fixed;
			bottom: 40vh;
			width: 100vw;
			font-size: $text-4xl;
			margin-left: auto;
			margin-right: auto;
			left: 0;
			right: 0;
			text-align: center;
		}
		&__loading {
			background-color: var(--primary-color);
			position: fixed;
			bottom: 50vh;
			width: 2rem;
			height: 2rem;
			left: 30vw;

			animation: loadinganim 2s infinite;

			@include screen(md) {
				animation: loadinganimdesktop 2s infinite;
			}
		}
	}

	@keyframes loadinganim {
		0% {
			left: calc(30vw - 2rem);
		}
		50% {
			left: 70vw;
		}
		100% {
			left: calc(30vw - 2rem);
		}
	}
	@keyframes loadinganimdesktop {
		0% {
			left: calc(40vw - 2rem);
		}
		50% {
			left: 60vw;
		}
		100% {
			left: calc(40vw - 2rem);
		}
	}
</style>
