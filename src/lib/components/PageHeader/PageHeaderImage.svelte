<script lang="ts">
	interface Props {
		background?: string;
		caption?: string;
		srcset?: string | null;
		sizes?: string | null;
	}

	let {
		background = '',
		caption = '',
		srcset = null,
		sizes = null
	}: Props = $props();
</script>

<div class="page-header-image">
	<img class="page-header-image__image" src={background} alt={caption} {srcset} {sizes} loading="lazy" >
</div>

<style lang="scss">
	@use '../../styles/global' as *;

	.page-header-image {
		background-color: var(--primary-bg-color);
		color: var(--primary-bg-color);
		border-radius: 20px 20px 0px 0px;
		overflow: hidden;

		:global(h1),
		:global(h2),
		:global(h3),
		:global(h4),
		:global(h5),
		:global(h6),
		:global(a),
		:global(p) {
			color: var(--primary-bg-color);
		}

		&__image {
			width: 100%;
			max-height: 37vw;
			object-fit: cover;
			@include screen(sm) {
				height: 236.8px;
			}
			@include screen(lg) {
				height: 284.14px;
			}
		}
	}
</style>
