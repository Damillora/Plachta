<script lang="ts">
	export let primary_tag: {
		accent_color: string;
		url: string;
		name: string;
	} | null = null;
	export let date = '';
	export let reading_time = '';
</script>

<div class="post-card__info">
	{#if primary_tag}
		{#if primary_tag.accent_color}
			<span class="post-card__tag-color" style="background-color: {primary_tag.accent_color};" />
		{/if}
		<a class="post-card__tag-name" href={primary_tag.url}>{primary_tag.name}</a>
	{/if}
	<p class="post-card__date">
		<time datetime={date}>
			{date}
		</time>
		<span class="bull">&bull;</span>
		{reading_time}
	</p>
</div>

<style lang="scss">
	@import '../../styles/global';

	.post-card {
		&__info {
			display: flex;
			flex-direction: row;
			align-items: center;
			margin-bottom: 0.5rem;
		}
		&__tag-color {
			display: inline-block;
			height: 1rem;
			width: 1rem;
			background-color: white;
			border-radius: 50%;
			margin-right: 0.5rem;
		}
		&__tag-name {
			font-size: $text-xs;
		}
		&__date {
			margin-left: auto;
			font-size: $text-xs;
			@include my(0);
		}
	}
</style>
