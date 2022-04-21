<template>
<div class="w-1/2 mx-auto">
    <img class="w-full" :src="skola.image" />
    <h1 class="text-5xl mb-8">{{skola.title}}</h1>
    <p class="mb-8">{{skola.description}}</p>
    <nuxt-content :document="skola"></nuxt-content>
</div>
</template>
<script>
export default {
    async asyncData({$content, params}) {
        
        let skola = await $content('skola/skola'+params.id).fetch()
        console.log(skola)

        return {
            skola
        }
    },
}
</script>