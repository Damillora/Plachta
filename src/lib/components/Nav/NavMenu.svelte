<script lang="ts">
	export let url = '';
	export let label = '';

    import NavMenuBase from "./NavMenuBase.svelte";
</script>
<NavMenuBase>
	<a href={url}>
		{ label }
	</a>
</NavMenuBase>