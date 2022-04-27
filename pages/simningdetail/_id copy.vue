<template>
<div class="w-1/2 mx-auto">
    <img class="w-full" :src="simning.image" />
    <h1 class="text-5xl mb-8">{{simning.title}}</h1>
    <p class="mb-8">{{simning.description}}</p>
    <nuxt-content :document="simning"></nuxt-content>
</div>
</template>
<script>
export default {
    async asyncData({$content, params}) {
        
        let simning = await $content('simning/simning'+params.id).fetch()
        console.log(simning)

        return {
            simning
        }
    },
}
</script>