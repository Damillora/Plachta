<script>
	import PostCard from '$lib/components/PostCard/PostCard.svelte';
	import Card from '$lib/components/Card/Card.svelte';
	import Container from '$lib/components/Container/Container.svelte';
	import Index from '$lib/components/PageTypes/Index.svelte';
	import CardTitle from '$lib/components/Card/CardTitle.svelte';
import CardContent from '$lib/components/Card/CardContent.svelte';
import CardDescription from '$lib/components/Card/CardDescription.svelte';
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
		<Card hasImage={false}>
			<CardContent>
				<CardTitle>Sophie!</CardTitle>
				<CardDescription>
					Sophie Neuenmuller!
				</CardDescription>
			</CardContent>
		</Card>
	</Index>
</Container>
