<div class="card__content">
	<slot />
</div>

<style lang="scss">
	@import '../../styles/global';

	.card__content {
		@include mx(1rem);
		@include my(1rem);

        display: flex;
        flex-direction: column;
        
		& > :global(*) {
			margin-top: 0rem;
			margin-bottom: 0.5rem;
		}
	}
</style>
