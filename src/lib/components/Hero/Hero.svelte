<script lang="ts">
	export let background = '';
	export let alt = '';
</script>

<div class="hero">
	<img class="hero__img" src={background} {alt} loading="lazy" />
	<!-- 
    {{#if background}} <img class="hero__img" srcset="{{img_url
        background size="s" }}
        300w, {{img_url
        background size="m" }} 600w" sizes="(max-width: 768px) 100vw, 35vw"
        src="{{img_url background size="m" }}" alt="{{title}}" loading="lazy">
    {{else}}
    <img class="hero__img" srcset="{{img_url @site.cover_image size="s"
        }} 300w, {{img_url
        @site.cover_image size="m" }} 600w" sizes="(max-width: 768px) 100vw,
        35vw"
        src="{{img_url @site.cover_image size="m" }}" alt="{{title}}"
        loading="lazy">

    {{/if}} -->
</div>

<style lang="scss">
	@import '../../styles/global';

	.hero {
		min-height: 150px;
		height: 25vh;
		z-index: 10;

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
	}
</style>
