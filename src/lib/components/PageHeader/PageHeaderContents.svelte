<script lang="ts">
</script>

<div class="page-header-contents">
	<slot />
</div>

<style lang="scss">
	@import '../../styles/global';

	.page-header-contents {
		@include py(1rem);
		@include px(1rem);
	}
</style>
