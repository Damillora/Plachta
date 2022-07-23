<script lang="ts">
	import PageHeader from '../PageHeader/PageHeader.svelte';

	export let accent_color: string | undefined;
	export let name = '';
	export let description: string | undefined;
</script>

<PageHeader>
	<p class="category-name">Tag</p>
	<div class="tag">
		<h1 class="tag__name">
			{#if accent_color}
				<span class="tag__color" style="background-color: {accent_color};" />
			{:else}
				<span class="tag__color" />
			{/if}
			{name}
		</h1>
		{#if description}
			<p class="tag__description">
				{description}
			</p>
		{/if}
	</div>
</PageHeader>

<style lang="scss">
	@import '../../styles/global';

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
			a {
				color: var(--primary-bg-color);
			}
		}
	}
</style>
