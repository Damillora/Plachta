<script lang="ts">
	interface Props {
		shown?: boolean;
		children?: import('svelte').Snippet;
	}

	let { shown = false, children }: Props = $props();
</script>

<nav class="nav" class:nav--shown={shown}>
	{@render children?.()}
</nav>

<style lang="scss">
	@import '../../styles/global';
	.nav {
		list-style-type: none;
		display: none;
		flex-direction: column;
		text-align: center;

		@include screen(md) {
			display: flex;
			flex-direction: row;
		}

		&--shown {
			display: flex;
			flex-direction: column;
		}
	}
</style>
