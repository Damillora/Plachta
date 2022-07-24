<script lang="ts">
	import Card from '$lib/components/Card/Card.svelte';

	export let feature_image = '';
	export let title = '';
	export let primary_tag: {
		accent_color: string;
		url: string;
		name: string;
	} | null = null;
	export let date = '';
	export let reading_time = '';
	export let url = '';
	export let excerpt = '';
	export let authors: {
		profile_image: string;
		url: string;
		name: string;
	}[] = [];
	export let readMore = false;
</script>

<Card>
	<article class="post-card">
		<div class="post-card__banner">
			{#if feature_image}
				<img class="post-card__img" src={feature_image} alt={title} loading="lazy" />
			{:else}
				<img class="post-card__img" src={feature_image} alt={title} loading="lazy" />
			{/if}
		</div>
		<div class="post-card__content">
			{#if primary_tag || date || reading_time}
				<div class="post-card__info">
					{#if primary_tag}
						{#if primary_tag.accent_color}
							<span
								class="post-card__tag-color"
								style="background-color: {primary_tag.accent_color};"
							/>
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
			{/if}
			<h2 class="post-card__title">
				<a href={url}>
					{title}
				</a>
			</h2>
			<p class="post-card__excerpt">
				{excerpt}
			</p>
			<div class="post-card__footer">
				{#if authors.length > 0}
					<div class="post-card__author">
						{#each authors as author}
							{#if author.profile_image}
								<a href={author.url}>
									<img
										src={author.profile_image}
										alt={author.name}
										class="post-card__author-image"
									/>
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
				{/if}
				{#if readMore}
					<p class="post-card__read-more">
						<a href={url}>Read more</a>
					</p>
				{/if}
			</div>
		</div>
	</article>
</Card>

<style lang="scss">
	@import '../../styles/global';

	.post-card {
		border-radius: 20px;
		@include shadow;
		margin-bottom: 2rem;
		display: grid;
		grid-template-rows: 150px 1fr;
		grid-template-columns: 1fr;

		@include screen(md) {
			grid-template-rows: 1fr;
			grid-template-columns: 300px 6fr;
		}

		&__banner {
			border-radius: 20px 20px 0px 0px;
			overflow: hidden;

			@include screen(md) {
				border-radius: 20px 0 0 20px;
			}
		}
		&__img {
			height: 0;
			min-height: 100%;
			width: 100%;
			object-fit: cover;
			object-position: center;
		}

		&__content {
			@include mx(1rem);
			@include my(1rem);

			@include screen(md) {
			}
		}

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

		&__title {
			margin-top: 0;
			margin-bottom: 0.5rem;
			font-size: $text-2xl;
		}
		&__excerpt {
			@include my(0.5rem);

			min-height: 5rem;
		}

		&__footer {
			margin-top: 0.5rem;
			display: flex;
			flex-direction: row;
			align-items: center;
		}

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
		&__read-more {
			@include my(0);
			margin-left: auto;
			font-size: $text-sm;
		}
	}
</style>
