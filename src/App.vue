<template>
	<main id="app">
		<music-player></music-player>
	</main>
</template>

<script>
import MusicPlayer from "./components/MusicPlayer.vue";

export default {
	name: "App",
	components: {
		MusicPlayer,
	},
};
</script>

<style lang="scss">
* {
	padding: 0;
	margin: 0;
	box-sizing: border-box;
}

// Style
$bg: #597ea4;

@mixin n-flat {
	border-radius: 5px;
	box-shadow: 21px 21px 47px #3b536c, -21px -21px 47px #77a9dc;
}

@mixin n-button {
	border-radius: 50%;
	width: 2rem;
	height: 2rem;
	border: none;
	outline: none;
	background: linear-gradient(145deg, #5f87af, #507194);
	box-shadow: 6px 6px 12px #44607d, -6px -6px 12px #6e9ccb;
}

@mixin n-button-pressed {	
	background: linear-gradient(145deg, #5f87af, #507194);
	box-shadow: 6px 6px 12px #44607d, -6px -6px 12px #6e9ccb;
}

body {
	background-color: $bg;
	color: white;
	padding: 1rem;

	#music-player {
		@include n-flat;
		padding: 1rem;
	}
}

.song__button {
	cursor: pointer;
	@include n-button;

	&:hover,
	&:focus,
	&:active {
	}
}
</style>
