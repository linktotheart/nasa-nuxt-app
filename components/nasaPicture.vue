<template>
  <div class="card">
	<figure class="block cursor-pointer mb-4 rounded max-h-[30rem] relative mih-h-[30rem] bg-base-200" @click="openFull" >
		<img :src="data.url" class="block object-fill" :alt="data.title">
	</figure>
	<h2 class="card-title font-medium mb-4	 text-3xl">
		{{ data.title }}
	</h2>
	<p class="text-gray-300 leading-5">
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