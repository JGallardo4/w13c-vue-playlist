<template>
	<section id="song-list">
		<ol id="song-list__container">
			<li v-for="(song, index) in songs" :key="index" class="song">
				<h1 class="song__title">{{ song.title }}</h1>
				<h1 class="song__artist">{{ song.artist }}</h1>
			</li>
		</ol>
	</section>
</template>

<script>
export default {
	name: "song-list",
	props: {
		songs: {
			type: Array
		}
	}	
}
</script>

<style lang="scss" scoped>
	#song-list {
		text-align: left;
		li {
			&:hover {
				background-color: beige;
			}
		}
	}
</style>