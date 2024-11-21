<script lang="ts">
	import type { Snippet } from 'svelte';
	
	import Nav from '../Nav/Nav.svelte';
	interface Props {
		title?: Snippet;
		nav?: Snippet;
	}

	let { title, nav }: Props = $props();

	let shown = $state(false);

	const toggleShown = () => (shown = !shown);
</script>

<header class="header" id="header">
	<div class="header__title">
		{@render title?.()}
	</div>
	<div class="header__nav">
		<a class="header__nav-button" id="menushow" onclick={toggleShown}>
			<span class="material-icons"> menu </span>
		</a>
		<Nav {shown}>
			{#if nav}{@render nav()}{:else}
				<!-- {{navigation}} -->
			{/if}
		</Nav>
	</div>
</header>

<style lang="scss">
	@use '../../styles/global' as *;

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
