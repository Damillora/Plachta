<footer class="footer">
	<slot />
</footer>

<style lang="scss">
	@import '../../styles/global';

	.footer {
		min-height: 3rem;
		background-color: var(--primary-color);
		color: var(--primary-bg-color);
		display: flex;
		align-items: center;
		@include px(1rem);
		@include py(1rem);
	}
</style>
