<script>
	import PostCard from '$lib/components/PostCard/PostCard.svelte';
	import Container from '$lib/components/Container/Container.svelte';
	import Index from '$lib/components/PageTypes/Index.svelte';
</script>

<Container>
	<Index>
		<PostCard
			authors={[
				{
					profile_image: 'https://images.nanao.moe/r/GDuirR.jpg',
					url: '/examples/post-page',
					name: 'Sophie Neuenmuller'
				}
			]}
			date="2022 November 2020"
			excerpt="Sophie!"
			feature_image="https://images.nanao.moe/r/7jETH3.png"
			primary_tag={{
				accent_color: '#3b7b9c',
				name: 'Sound Voltex',
				url: '/examples/post-page'
			}}
			reading_time="3 min"
			title="Sophie!"
			url="/examples/post-page"
		/>
		<PostCard
			authors={[
				{
					profile_image: 'https://images.nanao.moe/r/GDuirR.jpg',
					url: '/examples/post-page',
					name: 'Sophie Neuenmuller'
				}
			]}
			date="2022 November 2020"
			excerpt="Sophie!"
			feature_image="https://images.nanao.moe/r/7jETH3.png"
			primary_tag={{
				accent_color: '#3b7b9c',
				name: 'Sound Voltex',
				url: '/examples/post-page'
			}}
			reading_time="3 min"
			title="Sophie!"
			url="/examples/post-page"
		/>
		<PostCard
			authors={[
				{	
					profile_image: 'https://images.nanao.moe/r/GDuirR.jpg',
					url: '/examples/post-page',
					name: 'Sophie Neuenmuller'
				}
			]}
			date="2022 November 2020"
			excerpt="Sophie!"
			feature_image="https://images.nanao.moe/r/7jETH3.png"
			primary_tag={{
				accent_color: '#3b7b9c',
				name: 'Sound Voltex',
				url: '/examples/post-page'
			}}
			reading_time="3 min"
			title="Sophie!"
			url="/examples/post-page"
		/>
	</Index>
</Container>
