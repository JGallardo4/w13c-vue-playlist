<template>
	<div id="music-player">
		<song-list></song-list>
		<play-list></play-list>
	</div>
</template>

<script>
import SongList from "./SongList.vue";
import PlayList from "./PlayList.vue";

export default {
	name: "music-player",
	components: {
		SongList,
		PlayList
	},
	data: function () {
		return {
			songs: [
				{ title: "Rock Me Amadeus", artist: "Falco III" },
				{ title: "Ashes of Love (feat. Caroline Polachek)", artist:"Danny L Harle" },
				{ title: "Mirrors", artist: "Justin Timberlake" },
				{ title: "Tell It to My Heart", artist: "Taylor Dayne" },
				{ title: "Radioactive", artist: "MARINA" },
				{ title: "There's a Thug In My Life", artist: "Rihanna" },
				{ title: "Be With You", artist: "Enrique Iglesias" },
				{ title: "You Spin Me Round (Like a Record)", artist: "Dead or Alive" },
			]
		};
	}
}
</script>

<style>

</style>