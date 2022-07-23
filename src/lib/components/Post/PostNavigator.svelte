<script lang="ts">
	export let prev_post = {
		url: '',
		title: ''
	};
	export let next_post = {
		url: '',
		title: ''
	};
</script>

<div class="post-navigator-root">
	{#if prev_post}
		<a href={prev_post.url} class="post-navigator post-navigator--prev">
			<span class="material-icons post-navigator__icon">arrow_back</span>
			<div
				class="post-navigator__content
            post-navigator__content--prev"
			>
				<p class="post-navigator__indicator">Previous post</p>
				<p class="post-navigator__title">{prev_post.title}</p>
			</div>
		</a>
	{/if}
	<div class="post-navigator__separator" />
	{#if next_post}
		<a href={next_post.url} class="post-navigator post-navigator--next">
			<div
				class="post-navigator__content
            post-navigator__content--next"
			>
				<p class="post-navigator__indicator">Next post</p>
				<p class="post-navigator__title">{next_post.title}</p>
			</div>
			<span class="material-icons post-navigator__icon">arrow_forward</span>
		</a>
	{/if}
</div>

<style lang="scss">
	@import '../../styles/global';

	.post-navigator-root {
		@include mx(auto);

		@include screen(md) {
			max-width: 640px;
		}
		@include screen(lg) {
			max-width: 768px;
		}

		@include screen(md) {
			display: flex;
			flex-direction: row;
		}
	}

	.post-navigator {
		background-color: var(--primary-color);
		color: var(--primary-bg-color);
		border-radius: 20px;
		@include shadow;
		@include py(1rem);
		@include px(1rem);
		@include mx(0.5rem);
		@include transition;
		margin-bottom: 1rem;

		display: flex;
		flex-direction: row;
		align-items: center;

		@include screen(md) {
			width: 33%;
		}

		&:hover {
			text-decoration: none;
			background-color: var(--primary-bg-color);
			color: var(--primary-color);
		}

		&__content {
			flex-grow: 1;
			&--prev {
				margin-left: 0.5rem;
				text-align: left;
			}
			&--next {
				margin-right: 0.5rem;
				text-align: right;
			}

			p {
				@include my(0.25rem);
			}
		}
		&__separator {
			@include screen(md) {
				flex-grow: 1;
			}
		}
	}
</style>
