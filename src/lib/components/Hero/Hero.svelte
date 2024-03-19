<script lang="ts">
	export let background = '';
	export let alt = '';
	export let srcset: string | null = null;
	export let sizes: string | null = null;
	export let halfWidth = false;
	export let doubleHeight = false;
</script>

<div class="hero"  class:hero--half-width={halfWidth} class:hero--double-height={doubleHeight}>
	<img class="hero__img" src={background} {alt} {srcset} {sizes} loading="lazy"/>
	<slot/>
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

		&--double-height {
			min-height: 300px;
			height: 50vh;
			@include screen(md) {
				height: 80vh;
				min-height: 600px;
			}
		}
	}
</style>
