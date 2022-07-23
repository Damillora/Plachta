<script lang="ts">
	import Index from '../PageTypes/Index.svelte';

	export let accent_color = '';
	export let name = '';
	export let url = '';
</script>

<Index>
	<div class="post-related">
		<span class="post-related__header">More in</span>
		{#if accent_color}
			<span class="post-related__tag-color" style="background-color: {accent_color};" />
		{:else}
			<span class="post-related__tag-color" />
		{/if}
		<span class="post-related__tag-description">
			<a href={url}>{name}</a>
		</span>
	</div>
</Index>
<Index>
	<slot />
</Index>

<style lang="scss">
	@import '../../styles/global';

	.post-related {
		display: flex;
		flex-direction: row;
		align-items: center;

		@include px(0.5rem);
		&__header {
			margin-right: 0.5rem;
		}
		&__tag-color {
			display: inline-block;
			height: 2rem;
			width: 2rem;
			background-color: white;
			border-radius: 50%;
			margin-right: 0.5rem;
		}
		&__tag-description {
		}
	}
</style>
