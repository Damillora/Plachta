<script lang="ts">
	export let shown = false;
</script>

<nav class="nav" class:nav--shown={shown}>
	<slot />
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
