<slot />

<style lang="scss" global>
	@import '../../styles/global';

	/* ghost styles */
	.kg-card {
		@include py(1rem);
		@include my(2rem);
		@include mx(0);
		display: flex;
		flex-direction: column;
		align-items: center;
		object-fit: contain;
		position: relative;

		.kg-image {
			width: 100%;
		}

		figcaption {
			font-size: $text-sm;
			background: var(--bg-color);
			color: var(--highlight-color);
			padding: 0.25rem 1rem;
			border-radius: 1rem;
			margin-left: 0.5rem;
			margin-right: 0.5rem;
			text-align: center;
			@include transition;

			@include screen(md) {
				padding: 0.5rem 2rem;
			}
		}
	}
	.kg-width-wide .kg-image {
		min-width: 100vw;
		@include screen(md) {
			min-width: 115%;
		}
		@include screen(lg) {
			min-width: 125%;
		}
		@include screen(xl) {
			min-width: 140%;
		}
	}

	.kg-width-full .kg-image {
		min-width: 100vw;
	}
	.kg-gallery-container {
		min-width: 100vw;
		@include screen(md) {
			min-width: 115%;
		}
		@include screen(lg) {
			min-width: 125%;
		}
		@include screen(xl) {
			min-width: 140%;
		}
	}

	.kg-gallery-row {
		display: flex;
		flex-direction: row;
	}
	.kg-gallery-image {
		@include mx(0.25rem);
		flex: 1 1 0%;
	}

	.kg-bookmark-card {
		color: var(--text-color);
	}

	.kg-bookmark-container {
		@include transition;
		display: flex;
		flex-direction: row;
		justify-content: space-between;
		color: var(--text-color);
		border-left: 1rem solid var(--primary-color);
		background-color: var(--bg-color);
		&:hover {
			@include transition;
			background-color: var(--highlight-bg-color);
		}
	}
	.kg-bookmark-content {
		width: 66.6667%;
		padding: 1rem;
	}
	.kg-bookmark-thumbnail {
		position: relative;
		max-height: 100%;
		min-width: 33.3333%;
	}
	.kg-bookmark-thumbnail img {
		position: absolute;
		top: 0;
		left: 0;
		width: 100%;
		height: 100%;
		object-fit: cover;
	}
	.kg-bookmark-title {
		font-weight: 500;
	}
	.kg-bookmark-description {
		font-weight: 300;
		font-size: $text-sm;
		@include my(0.5rem);
	}
	.kg-bookmark-metadata {
		display: flex;
		flex-direction: row;
		align-items: flex-start;
		justify-content: flex-end;
		height: 1.5rem;
		@include my(1rem);
	}
	.kg-bookmark-icon {
		@include mx(0.5rem);
		height: 100%;
	}
	.kg-bookmark-author {
		font-size: $text-sm;
		color: var(--primary-color);
		overflow: hidden;
		text-overflow: ellipsis;
		white-space: nowrap;
	}
	.kg-bookmark-publisher {
		font-size: $text-sm;
		color: var(--primary-color);
		overflow: hidden;
		text-overflow: ellipsis;
		white-space: nowrap;
	}
</style>
