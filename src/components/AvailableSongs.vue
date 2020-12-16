<template>
	<section id="song-list">
		<header id="song-list__header">
			<h1>Available Songs</h1>
		</header>
		<ol id="song-list__container">
			<song-component 
				v-for="(song, index) in songs" 
				:key="index"
				:songInfo="song"
				:buttonAction="() => $emit('add-to-playlist', index)"
				class="song"
			>
				<i class="fa fa-plus" aria-hidden="true"></i>
			</song-component>
		</ol>
	</section>
</template>

<script>
import SongComponent from "./SongComponent.vue";

export default {
	name: "available-songs",

	props: {
		songs: {
			type: Array
		}
	},

	components: {
		SongComponent
	} 
}
</script>

<style lang="scss" scoped>
</style>