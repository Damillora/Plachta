<main class="post">
	<slot />
</main>

<style lang="scss">
	@import '../../styles/global';

	.post {
		@include mx(auto);

		@include screen(md) {
			max-width: 640px;
		}
		@include screen(lg) {
			max-width: 768px;
		}
	}
</style>
