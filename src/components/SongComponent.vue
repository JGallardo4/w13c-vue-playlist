<template>
	<li class="song">
		<h1 class="song__title">{{ songInfo.title }}</h1>
		<h1 class="song__artist">{{ songInfo.artist }}</h1>
		<button v-on:click="buttonInfo.action">
			{{buttonInfo.label}}
		</button>
	</li>
</template>

<script>
export default {
	name: "song-component",

	props: {
		songInfo: {
			type: Object
		},

		buttonInfo: {
			label: {
				type: String
			},

			action: {
				type: Function
			}
		}
	}
};
</script>

<style>
</style>