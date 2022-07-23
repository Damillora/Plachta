<script lang="ts">
	import PageHeader from '../PageHeader/PageHeader.svelte';

	export let profile_image = '';
	export let name = '';
	export let bio = '';
	export let website: string | undefined = undefined;
	export let twitter: string | undefined = undefined;
	export let facebook: string | undefined = undefined;
</script>

<PageHeader>
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
				<span class=""><a href={`https://twitter.com/${twitter}`} target="_blank" rel="noopener">Twitter</a></span>
			{/if}
			{#if facebook}
				<span class=""><a href={`${facebook}`} target="_blank" rel="noopener">Facebook</a></span>
			{/if}
		</p>
	</div>
</PageHeader>

<style lang="scss">
	@import '../../styles/global';

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
