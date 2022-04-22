<template>
<div class="w-full">
<header
  class="flex items-center justify-center h-screen mb-12 bg-fixed bg-center bg-cover first-img"
>
  <img class="static h-auto w-full self-end z-0" src="diagonalvy.svg" style="margin-bottom: -10px; padding: 10;"/>
</header>
<div class="max-w-lg m-auto">
  <Nuxt-Link to="/simning" class="mb-4 font-bold hover:underline"> 
   Simning
  </Nuxt-Link>
  <p class="mb-4">
    Jag simmar för Västeråssimsällskap, känt som VSS, och har genom åren klätrat mig i den nationella rankingen. Min hitills bästa prestation är en sjätte plats på ungdoms-sm vilket är något jag är väldigt stolt över.
  </p>
  <NuxtLink to="/simning" class="hover:underline mb-12">
    Läs om min sim karriär och följ mina senaste prestationer.
  </NuxtLink>
</div>
<img class="static h-auto w-full self-end z-0" src="diagonalvy.svg" style="position: absolute; margin-top: -5px; -moz-transform: scale(-1, -1); -o-transform: scale(-1, -1); -webkit-transform: scale(-1, -1); transform: scale(-1, -1);"/>
<section
  class="container flex items-center justify-center h-screen m-auto mb-12 bg-fixed bg-center bg-cover second-img"
>
<img class="static h-auto w-full self-end z-0" src="diagonalvy2.svg" style="margin-bottom: -5px; padding: 10;"/>
</section>
<div class="max-w-lg m-auto">
   <Nuxt-Link to="/skola" class="mb-4 font-bold hover:underline"> 
   Skola
  </Nuxt-Link>
  <p class="mb-4">
    Jag går på Abbs gymnasieskola och där läser jag programmet Teknikspets. 
  </p>
  <NuxtLink to="/skola" class="hover:underline mb-12">
    Läs om min skolgång och följ mina senaste projekt.
  </NuxtLink>
  </div>
<section
  class="container flex items-center justify-center h-screen m-auto mb-12 bg-fixed bg-center bg-cover third-img"
>
<img class="static h-auto w-full self-start z-0" src="diagonalvy2.svg" style="margin-top: -1px; -moz-transform: scale(-1, -1); -o-transform: scale(-1, -1); -webkit-transform: scale(-1, -1); transform: scale(-1, -1);"/>
<img class="static h-auto w-full self-end z-0" src="diagonalvy3.svg" style=" position: absolute; margin-bottom: -5px;"/>
</section>
<div class="max-w-lg m-auto">
  <Nuxt-Link to="/fritid" class="mb-4 font-bold hover:underline"> 
   Fritid
  </Nuxt-Link>
  <p class="mb-4">
    Följd med i min fritid och se vad jag gör nör jag inte är i skolan eller simmar.
  </p>
</div>
</div>
</template>

<style scoped>
.first-img {
  background-image: url("static/images/sumsimguld.png");
  max-width: 100vw;
}
.second-img {
  background-image: url("static/images/programering.png");
  max-width: 100vw;
}
.third-img {
  background-image: url("static/images/idregolf.jpg");
  max-width: 100vw;
} 
</style>

<script>
export default {
  name: "IndexPage",
};
</script>