<main class="index">
	<slot />
</main>

<style lang="scss">
	@import '../../styles/global';
	.index {
		@include my(2rem);
		@include px(1rem);
	}
</style>
