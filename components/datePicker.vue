<template>
  <div class="form-control">
	<!-- <label class="label">
		<span class="label-text">Date</span>
	</label> -->
	<label class="input-group input-group-sm">
		<span>Date</span>
		<input type="date" v-model="date" placeholder="select a date" @change="$emit('change', date)" class="input input-bordered" />
	</label>
</div>
</template>

<script>
export default {
	data() {
		return {
			date: ''
		}
	},
	methods: {
	}
}
</script>

<style>

</style>