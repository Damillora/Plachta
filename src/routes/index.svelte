<script>
	import Container from '$lib/components/Container/Container.svelte';

	import Post from '$lib/components/PageTypes/Post.svelte';
	import PostHeader from '$lib/components/Post/PostHeader.svelte';
	import PostMain from '$lib/components/Post/PostMain.svelte';
</script>

<Container>
	<Post>
		<PostHeader isPage={true} title="Plachta" />
		<PostMain comments={false}>
			<p>
				Welcome to documentation for Plachta, a Svelte component library based on Mare Serenitatis.
			</p>
			<p>Pages:</p>
			<ul>
				<li><a href="/examples/index-page">Index</a></li>
				<li><a href="/examples/post-page">Post</a></li>
				<li><a href="/examples/page-page">Page</a></li>
				<li><a href="/examples/tag-page">Tag</a></li>
				<li><a href="/examples/author-page">Author</a></li>
				<li><a href="/examples/card">Card</a></li>
			</ul>
		</PostMain>
	</Post>
</Container>
