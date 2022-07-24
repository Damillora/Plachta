<script>
	export let hasImage = false;
</script>

<div class="card" class:card--image={hasImage}>
	<slot />
</div>

<style lang="scss">
	@import '../../styles/global';

	.card {
		border-radius: 20px;
		@include shadow;
		margin-bottom: 2rem;
		display: flex;
		
		&--image {
			display: grid;
			grid-template-rows: 150px 1fr;
			grid-template-columns: 1fr;

			@include screen(md) {
				grid-template-rows: 1fr;
				grid-template-columns: 300px 6fr;
			}
		}
	}
</style>
