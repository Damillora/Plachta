<script lang="ts">
	import NavMenuBase from './NavMenuBase.svelte';
	import theme, { setTheme } from '../../../svelte-themes';

	let themeValue: string | undefined = 'light';
	theme.subscribe((val) => (themeValue = val.theme));

	let icon = 'brightness_high';
	function setDarkMode() {
		if (themeValue == 'dark') {
			icon = 'brightness_high';
		} else {
			icon = 'brightness_low';
		}
	}
	setDarkMode();

	function darkModeClick() {
		if (themeValue != 'dark') {
			setTheme("dark")
		} else {
			setTheme('light');
		}
		setDarkMode();
	}
</script>

<NavMenuBase>
	<span class="material-icons" id="dark-mode" on:click={darkModeClick}> {icon}</span>
</NavMenuBase>
