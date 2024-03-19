<script lang="ts">
	export let background = '';
	export let alt = '';
	export let srcset: string | null = null;
	export let sizes: string | null = null;
	export let halfWidth = false;
	export let contentSize: 'none' | 'short' | 'medium' | 'tall' = 'none';
</script>

<div
	class="hero"
	class:hero--half-width={halfWidth}
	class:hero--content-short={contentSize == 'short'}
	class:hero--content-medium={contentSize == 'medium'}
	class:hero--content-tall={contentSize == 'tall'}
>
	<img class="hero__img" src={background} {alt} {srcset} {sizes} loading="lazy" />
	<slot />
</div>

<style lang="scss">
	@import '../../styles/global';

	.hero {
		min-height: 150px;
		height: 25vh;
		z-index: 10;
		position: relative;
		width: 100%;

		@include screen(md) {
			height: 40vh;
			min-height: 300px;
		}

		&__img {
			height: 100%;
			width: 100%;
			object-fit: cover;
			object-position: center;
		}

		&--half-width {
			width: 100%;

			@include screen(md) {
				width: 50%;
			}
		}

		&--content-short {
			min-height: 150px;
			height: 150px;

			@include screen(md) {
				min-height: 150px;
				height: 150px;
			}
		}

		&--content-medium {
			min-height: 300px;
			height: 300px;

			@include screen(md) {
				min-height: 300px;
				height: 300px;
			}
		}

		&--content-tall {
			min-height: 500px;
			height: 500px;

			@include screen(md) {
				min-height: 500px;
				height: 500px;
			}
		}
	}
</style>
