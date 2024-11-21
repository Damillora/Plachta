<script lang="ts">
	import PageHeader from '../PageHeader/PageHeader.svelte';
	import PageHeaderContents from '../PageHeader/PageHeaderContents.svelte';
	import PageHeaderImage from '../PageHeader/PageHeaderImage.svelte';

	interface Props {
		background?: string;
		profile_image?: string;
		name?: string;
		bio?: string;
		website?: string | undefined;
		twitter?: string | undefined;
		facebook?: string | undefined;
	}

	let {
		background = '',
		profile_image = '',
		name = '',
		bio = '',
		website = undefined,
		twitter = undefined,
		facebook = undefined
	}: Props = $props();
</script>

<PageHeader>
	{#if background}
	<PageHeaderImage background={background}>
		
	</PageHeaderImage>
	{/if}
	<PageHeaderContents>
		<p class="category-name">Author</p>
		<div class="author">
			<h1 class="author__name">
				<img class="author__image" src={profile_image} alt={name} />
				{name}
			</h1>
			<p class="author__description">{bio}</p>
			<p class="author__description">
				{#if website}
					<span class=""><a href={website} target="_blank" rel="noopener">Website</a></span>
				{/if}
				{#if twitter}
					<span class=""
						><a href={`https://twitter.com/${twitter}`} target="_blank" rel="noopener">Twitter</a
						></span
					>
				{/if}
				{#if facebook}
					<span class=""><a href={`${facebook}`} target="_blank" rel="noopener">Facebook</a></span>
				{/if}
			</p>
		</div>
	</PageHeaderContents>
</PageHeader>

<style lang="scss">
	@use '../../styles/global' as *;

	.author {
		&__name {
			display: flex;
			flex-direction: row;
			align-items: center;
			color: var(--primary-bg-color);
		}
		&__image {
			display: inline-block;
			height: 4rem;
			width: 4rem;
			background-color: white;
			border-radius: 50%;
			margin-right: 1rem;
			object-fit: cover;
			object-position: center;
		}
		&__description {
			a {
				color: var(--primary-bg-color);
			}
		}
	}
</style>
