<div class="card">
	<slot />
</div>

<style lang="scss">
	@import '../../styles/global';

	.card {
		border-radius: 20px;
		@include shadow;
		margin-bottom: 2rem;
	}
</style>
