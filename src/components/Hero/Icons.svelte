<script>
	import AirMax from "$lib/icons/AirMax.svelte";
	import IconBeer from "~icons/ion/ios-beer";
	import IconMug from "~icons/game-icons/coffee-mug";
	import IconSpeaker from "~icons/material-symbols/speaker-outline";
	import IconCodeSlash from "~icons/ion/code-slash-sharp";
</script>

<p class="container">
	<span class="beer">
		<IconBeer />
	</span>
	<span class="coffee">
		<IconMug />
	</span>
	<span class="speaker">
		<IconSpeaker />
	</span>
	<span class="code">
		<IconCodeSlash />
	</span>
	<span class="air-max">
		<AirMax />
	</span>
</p>

<style>
	.container {
		font-size: x-large;
		display: flex;
		flex-direction: row;
		align-items: flex-end;
		justify-content: start;
	}

	.container span {
		margin-right: 20px;
		filter: drop-shadow(2px 2px 3px var(--background));
		transition: all 0.2s ease-out;
		color: var(--foreground);
	}

	.container span:hover {
		transform: translateY(-2px);
		filter: drop-shadow(2px 4px 3px var(--charcoal));
	}

	.air-max {
		margin-bottom: 2px;
	}

	.beer:hover {
		color: var(--yellow);
	}

	.coffee:hover {
		color: var(--green);
	}

	.speaker:hover {
		color: var(--purple);
	}

	.code:hover {
		color: var(--orange);
	}

	@media only screen and (max-width: 600px) {
		.container {
			justify-content: center;
		}
	}
</style>
