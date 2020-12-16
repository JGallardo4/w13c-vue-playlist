<template>
	<div>
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
	}
}
</script>

<style>

</style>