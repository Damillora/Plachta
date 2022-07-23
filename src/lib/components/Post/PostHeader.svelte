<script lang="ts">
	import PageHeader from '../PageHeader/PageHeader.svelte';

	export let isPage = false;

	export let title = '';
	export let primary_tag:
		| {
				accent_color: string;
				url: string;
				name: string;
		  }
		| undefined = undefined;
	export let date: string = '';
	export let reading_time = '';
	export let authors: { profile_image: string; url: string; name: string }[] | null = null;
</script>

<PageHeader>
	{#if isPage == false}
		<div class="post-header__info">
			{#if primary_tag}
				{#if primary_tag.accent_color}
					<span
						class="post-header__tag-color"
						style="background-color: {primary_tag.accent_color};"
					/>
				{/if}
				<span class="post-header__tag-name">
					<a href={primary_tag.url}>{primary_tag.name}</a>
				</span>
			{/if}
			<p class="post-header__date">
				<time datetime={date}>
					{date}
				</time>
				<span class="bull">&bull;</span>
				{reading_time}
			</p>
		</div>
	{/if}
	<h1 class="post-header__title">
		{title}
	</h1>
	{#if isPage == false}
		<div class="post-header__author">
			{#if authors}
				{#each authors as author}
					{#if author.profile_image}
						<a href={author.url}>
							<img src={author.profile_image} class="post-header__author-image" alt={author.name} />
						</a>
					{/if}
				{/each}
				<p class="post-header__author-name">
					{#if authors.length > 2}
						Multiple authors
					{:else}
						{#each authors as author}
							<a href={author.url} title={author.name}>{author.name}</a>
						{/each}
					{/if}
				</p>
			{/if}
		</div>
	{/if}
</PageHeader>

<style lang="scss">
	@import '../../styles/global';

	.post-header {
		&__info {
			display: flex;
			flex-direction: row;
			align-items: center;
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
			a {
				color: var(--primary-bg-color);
			}
		}
		&__date {
			margin-left: auto;
			font-size: $text-xs;
			@include my(0);
		}

		&__title {
			@include my(0.5rem);
			color: var(--primary-bg-color);
		}

		&__author {
			display: flex;
			flex-direction: row;
			align-items: center;
		}
		&__author-image {
			border-radius: 50%;
			height: 2rem;
			margin-right: 0.5rem;
			object-fit: contain;
			object-position: center;
		}
		&__author-name {
			@include my(0);
			font-size: $text-sm;
			a {
				color: var(--primary-bg-color);
			}
		}
	}
</style>
