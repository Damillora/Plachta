<script>
	import PostCard from '$lib/components/PostCard/PostCard.svelte';
	import Container from '$lib/components/Container/Container.svelte';
	import Index from '$lib/components/PageTypes/Index.svelte';
</script>

<Container>
	<Index>
		<PostCard
			feature_image="https://images.nanao.moe/r/7jETH3.png"
			title="Sophie!"
			url="/examples/post-page"
			excerpt="Sophie!"
		/>
		<PostCard
			feature_image="https://images.nanao.moe/r/7jETH3.png"
			title="Sophie!"
			url="/examples/post-page"
			excerpt="Sophie!"
		/>
		<PostCard
			feature_image="https://images.nanao.moe/r/7jETH3.png"
			title="Sophie!"
			url="/examples/post-page"
			excerpt="Sophie!"
		/>
	</Index>
</Container>
