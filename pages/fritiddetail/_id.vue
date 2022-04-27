<template>
  <div class="max-w-4xl flex items-center h-auto flex-wrap mx-auto my-32 lg:my-0 p-2">
    <div id="profile" class="w-full lg:w-3/5 rounded-lg lg:rounded-l-lg lg:rounded-r-none shadow-2xl bg-white opacity-75 mx-6 lg:mx-0">
		<div class="p-4 md:p-12 text-center lg:text-left">
			<img class="block lg:hidden rounded-full shadow-xl mx-auto -mt-16 h-48 w-48 bg-cover bg-center" :src="fritid.image">
			<h1 class="text-3xl font-bold pt-8 lg:pt-0">{{fritid.title}}</h1>
			<div class="mx-auto lg:mx-0 w-4/5 pt-3 border-b-2 border-green-500 opacity-25"></div>
			<p class="pt-4 text-base font-bold flex items-center justify-center lg:justify-start"><svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="12" r="10"></circle><polyline points="12 6 12 12 16 14"></polyline></svg>&nbsp;&nbsp;{{fritid.date}}</p>
			<p class="pt-4 text-base font-bold flex items-center justify-center lg:justify-start"><svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" viewBox="0 0 24 24" fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="12" cy="10" r="3"/><path d="M12 21.7C17.3 17 20 13 20 10a8 8 0 1 0-16 0c0 3 2.7 6.9 8 11.7z"/></svg>&nbsp;&nbsp;{{fritid.place}}</p>
            <p class="pt-8 text-sm"><nuxt-content :document="fritid"></nuxt-content></p>
			<div class="mt-6 pb-16 lg:pb-0 w-4/5 lg:w-full mx-auto flex flex-wrap items-center justify-between">
                <NuxtLink to="/fritid"><svg xmlns="http://www.w3.org/2000/svg" width="19" height="19" viewBox="0 0 24 24" fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M19 12H6M12 5l-7 7 7 7"/></svg></NuxtLink>
            </div>
		</div>
	</div>
	<div class="w-full lg:h-auto">
		<img :src="fritid.image" class="rounded-none lg:rounded-lg shadow-2xl hidden lg:block">
	</div>
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