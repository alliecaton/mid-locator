<template>
	<div>
		<div>
			<label>Point A</label>
			<input type="text" v-model="pointA" />
		</div>
		<div>
			<label>Point B</label>
			<input type="text" v-model="pointB" />
		</div>
		<div>
			<label>Type</label>
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
		}
	},
}
</script>
