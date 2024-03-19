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
		<h2>Hero Content</h2>
	</Post>
</Container>

<Hero background="https://images.nanao.moe/r/7jETH3.png">
	<HeroContent>
		<h1>Astesia Urbica</h1>
		<p>Star birb</p>
	</HeroContent>
</Hero>
<HeroList>

	<Hero background="https://images.nanao.moe/r/7jETH3.png" halfWidth contentSize="short">
		<HeroContent>
			<h1>Astesia Urbica</h1>
			<p>Star birb</p>
		</HeroContent>
	</Hero>
	<Hero background="https://images.nanao.moe/r/7jETH3.png" halfWidth contentSize="short">
		<HeroContent>
			<h1>Astesia Urbica</h1>
			<p>Star birb</p>
		</HeroContent>
	</Hero>
	<Hero background="https://images.nanao.moe/r/7jETH3.png" contentSize="medium">
		<HeroContent>
			<h1>Astesia Urbica</h1>
			<p>Star birb</p>
		</HeroContent>
	</Hero>
	<Hero background="https://images.nanao.moe/r/7jETH3.png" contentSize="tall">
		<HeroContent>
			<h1>Astesia Urbica</h1>
			<p>Star birb</p>
		</HeroContent>
	</Hero>
</HeroList>