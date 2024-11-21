<script lang="ts">
</script>

<div class="notice">
	<slot />
</div>

<style lang="scss">
	@import '../../styles/global';

	.notice {
		background: var(--primary-bg-color);
		color: var(--primary-color);
		padding: 1.25rem;
		border: 1px solid var(--primary-color);
		margin-bottom: 1rem;
	}
</style>
