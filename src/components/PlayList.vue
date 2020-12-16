<template>
	<section id="play-list">
		<ol id="play-list__container">
			<li v-for="(song, index) in songs" :key="index" class="song">
				<h1 class="song__title">{{ song.title }}</h1>
				<h1 class="song__artist">{{ song.artist }}</h1>
			</li>
		</ol>
	</section>
</template>

<script>
export default {
	name: "play-list",

	data: function () {
		return {
			songs: []
		};
	},

	methods: {
		
	}
}
</script>

<style>

</style>