<script lang="ts">
	export let url = '';
	export let title = '';
	export let excerpt = '';
</script>

<div class="search-result">
	<a href={url}><h2 class="search-result__title">{title}</h2></a>
	<p class="search-result__desc">{excerpt}</p>
</div>

<style lang="scss">
	@import '../../styles/global';
    
	.search-result {
		background-color: var(--bg-color);
		color: var(--text-color);
		border-radius: 20px;
		margin-bottom: 1rem;
		@include shadow;
		@include py(1rem);
		@include px(1rem);
	}
</style>
