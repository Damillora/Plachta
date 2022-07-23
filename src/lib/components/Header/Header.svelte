<script lang="ts">
	import Nav from '../Nav/Nav.svelte';

	let shown = false;

	const toggleShown = () => (shown = !shown);
</script>

<header class="header" id="header">
	<div class="header__title">
		<slot name="title" />
	</div>
	<div class="header__nav">
		<a class="header__nav-button" id="menushow" on:click={toggleShown}>
			<span class="material-icons"> menu </span>
		</a>
		<Nav {shown}>
			<slot name="nav">
				<!-- {{navigation}} -->
			</slot>
		</Nav>
	</div>
</header>

<style lang="scss">
	@import '../../styles/global';

	.header {
		display: flex;
		flex-direction: column;
		align-items: center;
		width: 100%;
		@include px(0.5rem);

		@include screen(md) {
			@include px(2rem);
			flex-direction: row;
		}

		&__title {
			font-size: $text-2xl;
			text-align: center;
			@include my(1rem);

			@include screen(md) {
				text-align: left;
				flex-grow: 1;
			}
		}
		&__nav {
			display: flex;
			flex-direction: column;
			text-align: center;
			margin-bottom: 1rem;

			@include screen(md) {
				@include my(1rem);
				flex-direction: row;
				align-items: center;
			}
		}
		&__nav-button {
			display: flex;
			flex-direction: column;
			justify-content: center;
			@include py(0.5rem);
			@include screen(md) {
				display: none;
			}
			&:hover,
			&:active,
			&:visited,
			&:focus {
				text-decoration: none;
			}
		}
	}
</style>
