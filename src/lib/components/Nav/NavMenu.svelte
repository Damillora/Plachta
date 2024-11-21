<script lang="ts">

    import NavMenuBase from "./NavMenuBase.svelte";
	interface Props {
		url?: string;
		label?: string;
	}

	let { url = '', label = '' }: Props = $props();
</script>
<NavMenuBase>
	<a href={url}>
		{ label }
	</a>
</NavMenuBase>