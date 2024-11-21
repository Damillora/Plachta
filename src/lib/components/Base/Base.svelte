<script>
	import SvelteTheme from '../../svelte-themes/SvelteTheme.svelte';
</script>

<SvelteTheme />

<slot />

<style lang="scss" global>
	@import '../../styles/global';
	@import '../../styles/utilities/normalize';

	html {
		font-family: 'Nunito', -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu,
			Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif !important;
	}
	:root,
	[data-theme='light'] {
		--text-color: #{$text-light};
		--bg-color: #{$bg-light};
		--primary-color: #{$primary-light};
		--primary-bg-color: #{$primary-bg-light};
		--secondary-color: #{$secondary-light};
		--secondary-bg-color: #{$secondary-bg-light};
		--highlight-color: #{$highlight-light};
		--highlight-bg-color: #{$highlight-bg-light};
	}

	[data-theme='dark'] {
		--text-color: #{$text-dark};
		--bg-color: #{$bg-dark};
		--primary-color: #{$primary-dark};
		--primary-bg-color: #{$primary-bg-dark};
		--secondary-color: #{$secondary-dark};
		--secondary-bg-color: #{$secondary-bg-dark};
		--highlight-color: #{$highlight-dark};
		--highlight-bg-color: #{$highlight-bg-dark};
	}

	@media (prefers-color-schme: dark) {
		:root:not[data-theme='light'] {
			--text-color: #{$text-dark};
			--bg-color: #{$bg-dark};
			--primary-color: #{$primary-dark};
			--primary-bg-color: #{$primary-bg-dark};
			--secondary-color: #{$secondary-dark};
			--secondary-bg-color: #{$secondary-bg-dark};
			--highlight-color: #{$highlight-dark};
			--highlight-bg-color: #{$highlight-bg-dark};
		}
	}

	body {
		color: var(--text-color);
		background-color: var(--bg-color);
	}

	.main {
		margin: 1rem;
		@include px(1rem);

		@include screen(sm) {
			@include px(2rem);
		}
		@include screen(md) {
			@include px(4rem);
		}
		@include screen(lg) {
			@include px(8rem);
		}
		@include screen(xl) {
			@include px(16rem);
		}
	}
	.page {
		width: 100%;
	}
	.main {
		margin-left: auto;
		margin-right: auto;
	}
	p {
		margin-bottom: 1rem;
		//@include my(1rem);
	}
	h1,
	h2,
	h3,
	h4,
	h5,
	h6 {
		margin-bottom: 0.5rem;
		font-weight: 300;
		color: var(--primary-color);
	}
	h1 {
		font-size: $text-2xl;

		@include screen(md) {
			font-size: $text-3xl;
		}
	}
	h2 {
		font-size: $text-xl;

		@include screen(md) {
			font-size: $text-2xl;
		}
	}
	h3 {
		font-size: $text-lg;

		@include screen(md) {
			font-size: $text-xl;
		}
	}
	h4 {
		font-size: $text-base;

		@include screen(md) {
			font-size: $text-lg;
		}
	}
	h5 {
		font-size: $text-sm;

		@include screen(md) {
			font-size: $text-base;
		}
	}
	h6 {
		font-size: $text-sm;

		@include screen(md) {
			font-size: $text-base;
		}
	}

	a {
		color: var(--primary-color);
		&:hover {
			text-decoration: underline;
		}
	}
	ul {
		list-style-type: disc;
		margin-bottom: 1rem;
		li {
			margin-left: 2rem;
		}
		li p {
			@include my(0rem);
		}
	}
	ol {
		list-style-type: decimal;
		li {
			margin-left: 2rem;
		}
		margin-bottom: 1rem;
	}
	code {
		background-color: var(--primary-bg-color);
		color: var(--primary-color);
		white-space: pre-wrap;
	}
	blockquote {
		border-left: 0.5rem solid var(--primary-color);
		@include my(2rem);
		padding: 0.5rem 0 0.5rem 2rem;
	}
	pre {
		background: var(--primary-bg-color);
		color: var(--primary-color);
		padding: 0.5rem;
		border: 1px solid var(--primary-color);
	}

	.card-list {
		display: flex;
		flex-direction: column;
	}
</style>
