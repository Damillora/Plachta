<script lang="ts">
</script>

<div class="hero-list">
	<slot/>
</div>

<style lang="scss">
	@import '../../styles/global';

	.hero-list {
		display: flex;
		flex-direction: row;
		flex-wrap: wrap;
	}
</style>
