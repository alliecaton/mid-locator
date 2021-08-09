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
		<button @click="searchPlaces">SEARCH</button>

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

	methods: {
		searchPlaces() {
			fetch(
				'https://maps.googleapis.com/maps/api/place/findplacefromtext/json?input=Museum%20of%20Contemporary%20Art%20Australia&inputtype=textquery&fields=photos,formatted_address,name,rating,opening_hours,geometry&key=AIzaSyDAUNbtyz2Ofwvctv_64BiiYIZX0oCSnak'
			)
				.then(r => r.json())
				.then(json => {
					console.log(json)
				})
		},
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
