<script lang="ts">
	import { navigating } from '$app/stores';

	import Base from '$lib/components/Base/Base.svelte';
	import Footer from '$lib/components/Footer/Footer.svelte';
	import Header from '$lib/components/Header/Header.svelte';
	import Hero from '$lib/components/Hero/Hero.svelte';
	import Nav from '$lib/components/Nav/Nav.svelte';
	import NavDarkMode from '$lib/components/Nav/NavDarkMode.svelte';
	import NavMenu from '$lib/components/Nav/NavMenu.svelte';
	import NavSearch from '$lib/components/Nav/NavSearch.svelte';
	import NavigationLoading from '$lib/components/NavigationLoading/NavigationLoading.svelte';
	import type { Snippet } from 'svelte';
	interface Props {
		children?: Snippet;
	}

	let { children }: Props = $props();

	let loading = $state(true);
	navigating.subscribe((x) => (loading = x != null));
</script>

<Base>
	<Header>
		{#snippet title()}
			
				<a href="/"> Plachta Theme Kit </a>
			
			{/snippet}
		{#snippet nav()}
			
				<NavMenu label="Home" url="/" />
				<NavDarkMode />
				<NavSearch />
			
			{/snippet}
	</Header>

	{@render children?.()}
	<Footer>
		<p>Copyright (c) 2021 Damillora</p>
	</Footer>
</Base>

<NavigationLoading {loading}/>

<style lang="scss">
	// Responsive embeds
	:global(.fluid-width-video-wrapper) {
		width: 100%;
		position: relative;
		padding: 0;
		:global(iframe),
		:global(object),
		:global(embed) {
			position: absolute;
			top: 0;
			left: 0;
			width: 100%;
			height: 100%;
		}
	}
</style>
