<template>
    <div class="h-screen">
        <header class="flex items-center justify-center h-screen mb-12 bg-fixed bg-center bg-cover custom-img">
            <div class="flex flex-wrap justify-center">
                <div @click="goTofritid(fritid.id)" class="w-80 p-2 m-4" v-for="fritid in fritid" :key="fritid.id">
                    <FritidListItem :item="fritid"> </FritidListItem>
                </div>
            </div>
        </header>
    </div>
</template>

<style scoped>
.custom-img {
  background-image: url(static/background\backgroundsimning.jpg);
}
</style>

<script>
export default {
  name: 'IndexPage',
  async asyncData({$content}) {
    let fritid = await $content('fritid').without(['body']).fetch()
    return {
      fritid
    }
  },
  methods: {
    goTofritid(id) {
      this.$router.push('/fritiddetail/'+id)
    }
  }
}
</script>
