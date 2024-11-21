<script lang="ts">
	interface Props {
		authors?: {
		profile_image: string;
		url: string;
		name: string;
	}[];
	}

	let { authors = [] }: Props = $props();
</script>

<div class="post-card__author">
	{#each authors as author}
		{#if author.profile_image}
			<a href={author.url}>
				<img src={author.profile_image} alt={author.name} class="post-card__author-image" />
			</a>
		{/if}
	{/each}
	<p class="post-card__author-name">
		{#if authors.length > 2}
			Multiple authors
		{:else}
			{#each authors as author}
				<a href={author.url} title={author.name}>{author.name}</a>
			{/each}
		{/if}
	</p>
</div>

<style lang="scss">
	@use '../../styles/global' as *;

	.post-card {
		&__author {
			display: flex;
			flex-direction: row;
			align-items: center;
		}
		&__author-image {
			border-radius: 50%;
			height: 2rem;
			object-fit: contain;
			object-position: center;
			margin-right: 0.5rem;
		}
		&__author-name {
			@include my(0);
			font-size: $text-sm;
		}
	}
</style>
