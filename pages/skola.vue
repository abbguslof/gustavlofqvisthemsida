<template>
    <div class="h-screen">
        <header class="flex items-center justify-center h-screen mb-12 bg-fixed bg-center bg-cover custom-img">
            <div class="flex flex-wrap justify-center">
                <div @click="goToSkola(skola.id)" class="w-80 p-2 m-4" v-for="skola in skola" :key="skola.id">
                    <SkolaListItem :item="skola"> </SkolaListItem>
                </div>
            </div>
        </header>
    </div>
</template>

<style scoped>
.custom-img {
  background-image: url(static\background\backgroundsimning.jpg);
}
</style>

<script>
export default {
  name: 'IndexPage',
  async asyncData({$content}) {
    let skola = await $content('skola').without(['body']).fetch()
    return {
      skola
    }
  },
  methods: {
    goToSkola(id) {
      this.$router.push('/skoladetail/'+id)
    }
  }
}
</script>
