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
				<li><a href="/examples/post-image-page">Post with Image</a></li>
				<li><a href="/examples/post-ghost-page">Post (Ghost)</a></li>
				<li><a href="/examples/post-image-ghost-page">Post with Image (Ghost)</a></li>
				<li><a href="/examples/page-page">Page</a></li>
				<li><a href="/examples/tag-page">Tag</a></li>
				<li><a href="/examples/author-page">Author</a></li>
				<li><a href="/examples/card">Card</a></li>
				<li><a href="/examples/hero">Hero</a></li>
				<li><a href="/examples/components">Other components</a></li>
			</ul>
		</PostMain>
	</Post>
</Container>
