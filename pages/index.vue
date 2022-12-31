<template>
  <div class="card">
    <div class="card-body px-0 md:px-4 lg:px-6 ">
      <div class="flex w-full justify-between mb-4">
        <date-picker @change="date = $event" />
        <button class="btn btn-primary" @click="fetchApod(date)">Go</button>
      </div>

      <loader v-if="isLoading" />
      <nasaPicture :data="imgData" v-else />
    </div>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  data() {
    return {
      imageURL: '',
      isLoading: true,
      date: '',
      imgData: {}
    }
  },
  async mounted() {
    await this.fetchApod();
  },

  methods: {
    async fetchApod(date) {
      this.isLoading = true
      let url = `https://api.nasa.gov/planetary/apod`
      url += '?api_key=G104rrn3edkbnCbmEFkQKUoM7qPT08alOw6AshtP'
      if (date) {
        url += `&date=${date}`
      }
      try {
        const data = await this.$axios.$get(url)
        if (data) this.imgData = data
      } catch (error) {
        console.log('error', error)
      }
      this.isLoading = false
    }
  }
}
</script>
