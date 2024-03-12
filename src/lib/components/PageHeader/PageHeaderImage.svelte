<script lang="ts">
	export let background = '';
	export let caption = '';
	export let srcset: string | null = null;
	export let sizes: string | null = null;
</script>

<div class="page-header-image">
	<img class="page-header-image__image" src={background} alt={caption} {srcset} {sizes} loading="lazy" >
</div>

<style lang="scss">
	@import '../../styles/global';

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
	}
</style>
