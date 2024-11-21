<script lang="ts">
	interface Props {
		image?: string;
		alt?: string;
	}

	let { image = '', alt = '' }: Props = $props();
</script>

<div class="card__banner">
	<img class="card__img" src={image} {alt} loading="lazy" />
</div>

<style lang="scss">
	@import '../../styles/global';

	.card__banner {
		border-radius: 20px 20px 0px 0px;
		overflow: hidden;

		@include screen(md) {
			border-radius: 20px 0 0 20px;
		}
	}
	.card__img {
		height: 0;
		min-height: 100%;
		width: 100%;
		object-fit: cover;
		object-position: center;
	}
</style>
