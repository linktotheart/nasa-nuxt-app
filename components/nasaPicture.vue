<template>
  <div class="card bg-base-100">
	<figure class="block cursor-pointer mb-4 rounded relative  lg:max-h-[30rem]  lg:min-h-[30rem]  max-h-[18srem]  min-h-[18srem] bg-base-200" @click="openFull" >
		<img :src="data.url" class="block object-fill" :alt="data.title">
	</figure>
	<h2 class=" card-title capitalize font-medium mb-4	 text-2xl lg:text-center">
		{{ data.title }}
	</h2>
	<p class="text-gray-300 font-mono leading-7">
		{{ data.explanation }}
	</p>
  </div>
</template>

<script>
export default {
	props: ['data'],
	methods: {
		openFull() {
			window.open(this.data.hdurl, '_blank')
		}
	}
}
</script>

<style>

</style>