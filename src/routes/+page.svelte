<script>
	import HeroImage from "../components/Hero/Image.svelte";
	import HeroText from "../components/Hero/Text.svelte";
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="AJ Bates portfolio" />
</svelte:head>

<div class="container">
	<HeroText />
	<HeroImage />
</div>

<style>
	.container {
		padding: 0;
		display: grid;
		grid-template-columns: repeat(3, 1fr);
		overflow: hidden;
		height: 100vh;
		background-image: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' width='100%25' height='100%25' viewBox='0 0 1200 800'%3E%3Cdefs%3E%3CradialGradient id='a' cx='0' cy='800' r='800' gradientUnits='userSpaceOnUse'%3E%3Cstop offset='0' stop-color='%23363848'/%3E%3Cstop offset='1' stop-color='%23363848' stop-opacity='0'/%3E%3C/radialGradient%3E%3CradialGradient id='b' cx='1200' cy='800' r='800' gradientUnits='userSpaceOnUse'%3E%3Cstop offset='0' stop-color='%23545c7e'/%3E%3Cstop offset='1' stop-color='%23545c7e' stop-opacity='0'/%3E%3C/radialGradient%3E%3CradialGradient id='c' cx='600' cy='0' r='600' gradientUnits='userSpaceOnUse'%3E%3Cstop offset='0' stop-color='%23474e6b'/%3E%3Cstop offset='1' stop-color='%23474e6b' stop-opacity='0'/%3E%3C/radialGradient%3E%3CradialGradient id='d' cx='600' cy='800' r='600' gradientUnits='userSpaceOnUse'%3E%3Cstop offset='0' stop-color='%2344475a'/%3E%3Cstop offset='1' stop-color='%2344475a' stop-opacity='0'/%3E%3C/radialGradient%3E%3CradialGradient id='e' cx='0' cy='0' r='800' gradientUnits='userSpaceOnUse'%3E%3Cstop offset='0' stop-color='%23282a36'/%3E%3Cstop offset='1' stop-color='%23282a36' stop-opacity='0'/%3E%3C/radialGradient%3E%3CradialGradient id='f' cx='1200' cy='0' r='800' gradientUnits='userSpaceOnUse'%3E%3Cstop offset='0' stop-color='%236272a4'/%3E%3Cstop offset='1' stop-color='%236272a4' stop-opacity='0'/%3E%3C/radialGradient%3E%3C/defs%3E%3Crect fill='url(%23a)' width='1200' height='800'/%3E%3Crect fill='url(%23b)' width='1200' height='800'/%3E%3Crect fill='url(%23c)' width='1200' height='800'/%3E%3Crect fill='url(%23d)' width='1200' height='800'/%3E%3Crect fill='url(%23e)' width='1200' height='800'/%3E%3Crect fill='url(%23f)' width='1200' height='800'/%3E%3C/svg%3E");
		background-attachment: fixed;
		background-size: cover;
	}

	@media only screen and (max-width: 600px) {
		.container {
			grid-column: 1 / span 3;
		}
	}
</style>
