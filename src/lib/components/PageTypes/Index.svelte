<main class="index">
	<slot />
</main>

<style lang="scss">
	@import '../../styles/global';
	.index {
		@include my(2rem);
		@include mx(1rem);
	}
</style>
