<template>
	<div class="main-container">
		<div class="card">
			<label>Point A </label>
			<input type="text" v-model="pointA" />
		</div>
		<div class="card">
			<label>Point B </label>
			<input type="text" v-model="pointB" />
		</div>
		<div class="card">
			<label>Type </label>
			<input type="text" v-model="type" />
		</div>
		<button>SEARCH</button>

		<div>{{ pointA }}</div>
		<div>{{ pointB }}</div>
		<div>{{ type }}</div>
	</div>
</template>

<script>
export default {
	name: 'location-input',

	data() {
		return {
			pointA: '',
			pointB: '',
			type: '',
			pointALat: '',
			pointBLat: '',
		}
	},
}
</script>

<style scoped>
.main-container {
	display: flex;
	flex-flow: column wrap;
	justify-content: center;
	align-items: center;
}

.card {
	background-color: aliceblue;
	width: 40%;
	margin: 5px;
	padding: 5px;
}
</style>
