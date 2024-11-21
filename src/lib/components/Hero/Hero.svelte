<script lang="ts">
	import type { Snippet } from 'svelte';
	
	interface Props {
		background?: string;
		alt?: string;
		srcset?: string | null;
		sizes?: string | null;
		halfWidth?: boolean;
		contentSize?: 'none' | 'short' | 'medium' | 'tall';
		children?: Snippet;
	}

	let {
		background = '',
		alt = '',
		srcset = null,
		sizes = null,
		halfWidth = false,
		contentSize = 'none',
		children
	}: Props = $props();
</script>

<div
	class="hero"
	class:hero--half-width={halfWidth}
	class:hero--content-short={contentSize == 'short'}
	class:hero--content-medium={contentSize == 'medium'}
	class:hero--content-tall={contentSize == 'tall'}
>
	<img class="hero__img" src={background} {alt} {srcset} {sizes} loading="lazy" />
	{@render children?.()}
</div>

<style lang="scss">
	@use '../../styles/global' as *;

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
