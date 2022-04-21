<template>
    <div class="h-screen">
        <header class="flex items-center justify-center h-screen mb-12 bg-fixed bg-center bg-cover custom-img">
            <div class="flex flex-wrap justify-center">
                <div @click="goTosimning(simning.id)" class="w-80 p-2 m-4" v-for="simning in simning" :key="simning.id">
                    <SimningListItem :item="simning"> </SimningListItem>
                </div>
            </div>
        </header>
    </div>
</template>

<style scoped>
.custom-img {
  background-image: url(../Assets\Background\backgroundsimning.jpg);
}
</style>

<script>
export default {
  name: 'IndexPage',
  async asyncData({$content}) {
    let simning = await $content('simning').without(['body']).fetch()
    return {
      simning
    }
  },
  methods: {
    goTosimning(id) {
      this.$router.push('/simningdetail/'+id)
    }
  }
}
</script>
