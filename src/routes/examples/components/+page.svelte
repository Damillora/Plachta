<script>
	import PostCard from '$lib/components/PostCard/PostCard.svelte';
	import Container from '$lib/components/Container/Container.svelte';
	import Index from '$lib/components/PageTypes/Index.svelte';
	import Notice from '$lib/components/Notice/Notice.svelte';
	import Post from '$lib/components/PageTypes/Post.svelte';
</script>

<Container>
	<Index>
		<Post>
			<h2>Notice</h2>
			<Notice>
				This page is a <strong>work-in-progress</strong>. Contributions are welcome!
			</Notice>
		</Post>
	</Index>
</Container>
