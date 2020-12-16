<template>
	<section id="song-list">
		<ol id="song-list__container">
			<song-component 
				v-for="(song, index) in songs" 
				:key="index"
				:songInfo="song"
				:buttonInfo="{
					label: 'Add to playlist',
					action: () => {
						$emit('add-to-playlist', index);
					}
				}"
				class="song">
			</song-component>
		</ol>
	</section>
</template>

<script>
import SongComponent from "./SongComponent.vue";

export default {
	name: "song-list",

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