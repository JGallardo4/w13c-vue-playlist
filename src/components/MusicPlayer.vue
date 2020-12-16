<template>
	<div id="music-player">
		<song-list 
			id="song-list"
			class="song-list"
			:songs="songsAvailable"			
			v-on:add-to-playlist="addToPlaylist($event)">
		</song-list>

		<play-list 
			id="play-list"
			class="song-list"
			:songs="playList"
			v-on:remove-from-playlist="removeFromPlaylist($event)">
		</play-list>
	</div>
</template>

<script>
import SongList from "./SongList";
import PlayList from "./PlayList";

export default {
	name: "music-player",

	components: {
		SongList,
		PlayList
	},

	methods: {
		addToPlaylist(aId) {
			this.playList.push(this.songsAvailable[aId]);
			this.songsAvailable.splice(aId, 1);
			console.log(`Adding ${this.songsAvailable[aId].title} at ${aId}`);
		},

		removeFromPlaylist(aId) {
			this.songsAvailable.push(this.playList[aId]);
			this.playList.splice(aId, 1);
			console.log(`Removing ${this.playList[aId].title} at ${aId}`);
		}
	},

	data: function () {
		return {
			songsAvailable: [
				{ title: "Rock Me Amadeus", artist: "Falco III" },
				{ title: "Ashes of Love (feat. Caroline Polachek)", artist:"Danny L Harle" },
				{ title: "Mirrors", artist: "Justin Timberlake" },
				{ title: "Tell It to My Heart", artist: "Taylor Dayne" },
				{ title: "Radioactive", artist: "MARINA" },
				{ title: "There's a Thug In My Life", artist: "Rihanna" },
				{ title: "Be With You", artist: "Enrique Iglesias" },
				{ title: "You Spin Me Round (Like a Record)", artist: "Dead or Alive" },
			],

			playList: []
		};
	}
}
</script>

<style lang="scss">
	#music-player {
		display: grid;
		grid-template-columns: 1fr 1fr;
			#song-list {
				grid-column: 1;
			}
			#play-list {
				grid-column: 2;
			}
	}

	.song-list {
		text-align: left;
		li {
			&:hover {
				background-color: beige;
			}
		}
	}
</style>