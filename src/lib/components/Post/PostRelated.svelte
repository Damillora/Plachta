<script lang="ts">
	import Index from '../PageTypes/Index.svelte';

	interface Props {
		accent_color?: string;
		name?: string;
		url?: string;
		children?: import('svelte').Snippet;
	}

	let {
		accent_color = '',
		name = '',
		url = '',
		children
	}: Props = $props();
</script>

<Index>
	<div class="post-related">
		<span class="post-related__header">More in</span>
		{#if accent_color}
			<span class="post-related__tag-color" style="background-color: {accent_color};"></span>
		{:else}
			<span class="post-related__tag-color"></span>
		{/if}
		<span class="post-related__tag-description">
			<a href={url}>{name}</a>
		</span>
	</div>
</Index>
<Index>
	{@render children?.()}
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
	}
</style>
