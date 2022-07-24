<script lang="ts">
</script>

<div class="page-header">
	<slot />
</div>

<style lang="scss">
	@import '../../styles/global';

	.page-header {
		background-color: var(--primary-color);
		color: var(--primary-bg-color);
		border-radius: 0px 0px 20px 20px;
		margin-bottom: 1rem;
		@include mx(0.5rem);
		@include py(1rem);
		@include px(1rem);
		@include shadow;

		:global(h1),
		:global(h2),
		:global(h3),
		:global(h4),
		:global(h5),
		:global(h6),
		:global(a),
		:global(p) {
			color: var(--primary-bg-color);
		}
	}
</style>
