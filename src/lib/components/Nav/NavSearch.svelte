<script lang="ts">
	import { createEventDispatcher } from 'svelte';

	const dispatch = createEventDispatcher();

	const doSearch = (event: any) => {
		dispatch('search', {
			query: event.target.value
		});
	};
</script>

<li class="nav-search">
	<input
		class="nav-search-box"
		type="text"
		name="search"
		id="search-query"
		on:input={doSearch}
	/>
	<span class="material-icons nav-search-icon"> search </span>
</li>

<style lang="scss">
	@import '../../styles/global';

	.nav-search {
		position: relative;
		height: 2.5rem;
		border-radius: 20px;
		@include shadow;
	}
	.nav-search-box {
		height: 100%;
		width: 100%;
		border-radius: 20px;
		appearance: none;
		background-color: var(--bg-color);
		text-align: left;
		vertical-align: center;
		@include px(1rem);
		padding-right: 2.5rem;

		&:focus-visible {
			outline: none;
		}
	}
	.nav-search-icon {
		position: absolute;
		right: 0.5rem;
		top: 0.5rem;
		vertical-align: center;
		display: flex;
	}
</style>
