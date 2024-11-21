<script lang="ts">
	interface Props {
		comments?: Snippet;
		children?: Snippet;
	}

	let { comments, children }: Props = $props();
</script>

<div class="post-main">
	<div class:post-main__content={true} class:post-main__with-comments={comments} class:post-main__without-comments={!comments}>
		{@render children?.()}
	</div>
	{#if comments}
		<div class="post-main__comments">
			<h1 class="post-main__comments-title">Comments</h1>

			{@render comments?.()}
		</div>
	{/if}
</div>

<style lang="scss">
	@use '../../styles/global' as *;

	.post-main {
		background-color: var(--bg-color);
		color: var(--text-color);
		border-radius: 20px;
		margin-bottom: 1rem;
		@include mx(0.5rem);
		@include shadow;

		&__content {
			padding-bottom: 0.1rem;
			padding-top: 1rem;
			@include px(1rem);
			background-color: var(--bg-color);
			color: var(--text-color);
		}
		&__with-comments {
			border-radius: 20px 20px 0px 0px;
		}
		&__without-comments {
			border-radius: 20px;
		}
		&__comments {
			@include py(1rem);
			@include px(1rem);
			border-radius: 0px 0px 20px 20px;
			background-color: var(--primary-color);
			color: var(--primary-bg-color);
		}
		&__comments-title {
			color: var(--primary-bg-color);
			@include my(0.25rem);
		}
	}
</style>
