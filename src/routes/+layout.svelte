<!-- 
	Name: _layout
	Description: Base layout for all views. 
	Notes:
-->

<script lang="ts">
	import Topbar from '$lib/components/Topbar.svelte';
</script>

<div id="theme-container">
	<div id="app-content">
		<Topbar />
		<main>
			<slot />
		</main>
	</div>
</div>

<style lang="scss">
	@import '../theme/_vars.scss';

	main {
		font-family: $brandFont;
		flex: 1;
		display: block;
		width: 100%;
		max-width: 1024px;
		margin: 0 auto;
		box-sizing: border-box;
	}
</style>
