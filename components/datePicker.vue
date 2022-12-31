<template>
  <div class="form-control">
	<!-- <label class="label">
		<span class="label-text">Date</span>
	</label> -->
	<label class="input-group">
		<span>Date</span>
		<input type="date" v-model="date" @change="$emit('change', date)" class="input input-bordered" />
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