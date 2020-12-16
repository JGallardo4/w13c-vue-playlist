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
	box-shadow: 21px 21px 47px #3b536c, -21px -21px 47px #77a9dc;
}

body {
	background-color: $bg;
	color: white;
	padding: 1rem;

	#music-player {
		@include n-flat;
		padding: 1rem;
		border-radius: 5px;
	}
}
</style>
