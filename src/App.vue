<template>
	<div>
		<!-- <img alt="Vue logo" src="./assets/logo.png" /> -->
		<location-input></location-input>
	</div>
</template>

<script>
import LocationInput from './components/LocationInput.vue'

export default {
	name: 'App',
	components: {
		LocationInput,
	},
}
</script>

<style>
#app {
	font-family: Avenir, Helvetica, Arial, sans-serif;
	-webkit-font-smoothing: antialiased;
	-moz-osx-font-smoothing: grayscale;
	text-align: center;
	color: #2c3e50;
	margin-top: 60px;
}
</style>
