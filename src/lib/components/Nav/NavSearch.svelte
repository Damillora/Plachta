<script lang="ts">
	export let searchValue = "";
</script>

<li class="nav-search">
	<input class="nav-search-box" type="text" name="search" id="search-query" bind:value={searchValue} />
	<span class="material-icons nav-search-icon"> search </span>
</li>

<style lang="scss">
    @import "../../styles/global";
    
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
