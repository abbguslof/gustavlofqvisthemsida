<template>
<div class="w-1/2 mx-auto">
    <img class="w-full" :src="fritid.image" />
    <h1 class="text-5xl mb-8">{{fritid.title}}</h1>
    <p class="mb-8">{{fritid.description}}</p>
    <nuxt-content :document="fritid"></nuxt-content>
</div>
</template>
<script>
export default {
    async asyncData({$content, params}) {
        
        let fritid = await $content('fritid/fritid'+params.id).fetch()
        console.log(fritid)

        return {
            fritid
        }
    },
}
</script>