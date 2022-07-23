<script lang="ts">
	export let comments = true;
</script>

<div class="post-main">
	<div class:post-main__content={comments == true} class:post-main__single={comments == false}>
		<slot />
	</div>
	{#if comments == true}
		<div class="post-main__comments">
			<h1 class="post-main__comments-title">Comments</h1>

			<slot name="comments" />
		</div>
	{/if}
</div>

<style lang="scss">
	@import '../../styles/global';

	.post-main {
		background-color: var(--bg-color);
		color: var(--text-color);
		border-radius: 20px;
		margin-bottom: 1rem;
		@include mx(0.5rem);
		@include shadow;

		&__content {
			@include py(1rem);
			@include px(1rem);
			border-radius: 20px 20px 0px 0px;
			background-color: var(--bg-color);
			color: var(--text-color);
		}
		&__single {
			@include py(1rem);
			@include px(1rem);
			border-radius: 20px;
			background-color: var(--bg-color);
			color: var(--text-color);
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
