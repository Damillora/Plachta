<script lang="ts">
	import Card from '$lib/components/Card/Card.svelte';
	import CardBanner from '../Card/CardBanner.svelte';
	import CardContent from '../Card/CardContent.svelte';
	import CardDescription from '../Card/CardDescription.svelte';
	import CardFooter from '../Card/CardFooter.svelte';
	import CardTitle from '../Card/CardTitle.svelte';
	import PostCardAuthor from './PostCardAuthor.svelte';
	import PostCardInfo from './PostCardInfo.svelte';

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
	export let readMore = true;
</script>

<Card hasImage={true}>
	<CardBanner image={feature_image} alt={title} />
	<CardContent>
		{#if primary_tag || date || reading_time}
			<PostCardInfo {primary_tag} {date} {reading_time} />
		{/if}
		<CardTitle>
			<a href={url}>
				{title}
			</a>
		</CardTitle>
		<CardDescription>
			<div class="post-card__excerpt">
				{excerpt}
			</div>
		</CardDescription>
		<CardFooter>
			{#if authors.length > 0}
				<PostCardAuthor {authors} />
			{/if}
			{#if readMore}
				<p class="post-card__read-more">
					<a href={url}>Read more</a>
				</p>
			{/if}
		</CardFooter>
	</CardContent>
</Card>

<style lang="scss">
	@import '../../styles/global';

	.post-card {
		&__read-more {
			@include my(0);
			margin-left: auto;
			font-size: $text-sm;
		}
        &__excerpt {
            min-height: 5rem;
        }
	}
</style>
