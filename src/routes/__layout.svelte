<script>
	import Base from '$lib/components/Base/Base.svelte';
	import Footer from '$lib/components/Footer.svelte/Footer.svelte';
	import Header from '$lib/components/Header/Header.svelte';
	import Hero from '$lib/components/Hero/Hero.svelte';
	import Nav from '$lib/components/Nav/Nav.svelte';
	import NavDarkMode from '$lib/components/Nav/NavDarkMode.svelte';
	import NavMenu from '$lib/components/Nav/NavMenu.svelte';
	import NavSearch from '$lib/components/Nav/NavSearch.svelte';
</script>

<Base>
	<Header>
		<svelte:fragment slot="title">
			<a href="/"> Plachta Theme Kit </a>
		</svelte:fragment>
        <svelte:fragment slot="nav">
			<NavMenu label="Home" url="/" />
			<NavDarkMode />
			<NavSearch />

        </svelte:fragment>
	</Header>
	<Hero background="https://images.nanao.moe/r/7jETH3.png" />

	<slot />
	<Footer>
		<p>Copyright (c) 2021 Damillora</p>
	</Footer>
</Base>
