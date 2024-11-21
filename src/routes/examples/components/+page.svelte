<script>
	import PostCard from '$lib/components/PostCard/PostCard.svelte';
	import Container from '$lib/components/Container/Container.svelte';
	import Index from '$lib/components/PageTypes/Index.svelte';
	import Notice from '$lib/components/Notice/Notice.svelte';
	import Post from '$lib/components/PageTypes/Post.svelte';
	import HeroContent from '$lib/components/Hero/HeroContent.svelte';
	import Hero from '$lib/components/Hero/Hero.svelte';
	import HeroList from '$lib/components/Hero/HeroList.svelte';
</script>

<Container>
	<Post>
		<h2>Notice</h2>
		<Notice>
			This page is a <strong>work-in-progress</strong>. Contributions are welcome!
		</Notice>
	</Post>
</Container>
