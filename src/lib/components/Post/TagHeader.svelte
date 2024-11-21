<script lang="ts">
	import PageHeader from '../PageHeader/PageHeader.svelte';
	import PageHeaderContents from '../PageHeader/PageHeaderContents.svelte';
	import PageHeaderImage from '../PageHeader/PageHeaderImage.svelte';

	interface Props {
		background?: string;
		accent_color: string | undefined;
		name?: string;
		description: string | undefined;
	}

	let {
		background = '',
		accent_color,
		name = '',
		description
	}: Props = $props();
</script>

<PageHeader>
	{#if background}
	<PageHeaderImage background={background}>
		
	</PageHeaderImage>
	{/if}
	<PageHeaderContents>
		<p class="category-name">Tag</p>
		<div class="tag">
			<h1 class="tag__name">
				{#if accent_color}
					<span class="tag__color" style="background-color: {accent_color};"></span>
				{:else}
					<span class="tag__color"></span>
				{/if}
				{name}
			</h1>
			{#if description}
				<p class="tag__description">
					{description}
				</p>
			{/if}
		</div>
	</PageHeaderContents>
</PageHeader>

<style lang="scss">
	@use '../../styles/global' as *;

	.tag {
		&__name {
			display: flex;
			flex-direction: row;
			align-items: center;
			color: var(--primary-bg-color);
		}
		&__color {
			display: inline-block;
			height: 2rem;
			width: 2rem;
			background-color: white;
			border-radius: 50%;
			margin-right: 1rem;
		}
		&__description {
			:global(a) {
				color: var(--primary-bg-color);
			}
		}
	}
</style>
