<template>
  <div>

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <script src='https://kit.fontawesome.com/a076d05399.js'></script>
    <link href="https://unpkg.com/tailwindcss@^1.0/dist/tailwind.min.css" rel="stylesheet">
    <script src="https://cdn.jsdelivr.net/gh/alpinejs/alpine@v2.x.x/dist/alpine.min.js" defer></script>
    <link href="https://fonts.googleapis.com/css?family=Source+Sans+Pro:wght@200|Baloo+Tamma+2|Roboto&display=swap"
        rel="stylesheet">
</head>

    <div class="font-sans antialiased fixed top-0 m-0 w-full z-10" id="app">
      <nav class="flex p-6 fixed items-center justify-between flex-wrap w-screen" id="Header">
        <div class="flex items-center flex-no-shrink text-white mr-6">
          <img class="fill-current h-8 w-8 mr-2" width="54" height="54" viewBox="0 0 54 54" src="favicon.svg" />
          <NuxtLink to="/" class="font-semibold text-xl tracking-tight">gustavlofqvist.se</NuxtLink>
        </div>
        <div class="block sm:hidden">
          <button @click="toggle()" class="flex items-center px-3 py-2 border rounded text-white border-teal-light hover:text-white hover:border-white">
            <svg class="fill-current h-3 w-3" viewBox="0 0 20 20" xmlns="http://www.w3.org/2000/svg"><title>Menu</title><path d="M0 3h20v2H0V3zm0 6h20v2H0V9zm0 6h20v2H0v-2z"/></svg>
          </button>
        </div>
        <div :class="'hidden'" class="w-full flex-grow sm:flex sm:items-center sm:w-auto" id="menu">
          <div class="text-sm sm:flex-grow">
            <NuxtLink to="/simning" class="no-underline block mt-4 sm:inline-block sm:mt-0 text-white hover:underline hover:text-red-300 mr-4">
              Simning
            </NuxtLink>
            <NuxtLink to="/skola" class="no-underline block mt-4 sm:inline-block sm:mt-0 text-white hover:underline hover:text-red-300 mr-4">
              Skola
            </NuxtLink>
            <NuxtLink to="/fritid" class="no-underline block mt-4 sm:inline-block sm:mt-0 text-white hover:underline hover:text-red-300">
              Fritid
            </NuxtLink>
          </div>
          <div>
            <a href="https://github.com/abbguslof/bloggproject" class="no-underline inline-block text-sm px-4 py-2 leading-none border rounded text-white border-white hover:border-transparent hover:text-black hover:bg-white mt-4 sm:mt-0">
              GitHub
            </a>
          </div>
        </div>
      </nav>
    </div>
      <div @click="closenav()"> 
        <nuxt class="z-0"/>
      </div>

    <!-- Footer section -->
    <div class="bottom-0 bg-cover bg-center" style="-moz-box-shadow: 3px 3px 5px 6px #ccc; -webkit-box-shadow: 3px 3px 5px 6px #ccc; box-shadow: 3px 3px 5px 6px #ccc; background-image: url('https://image.freepik.com/free-photo/abstract-black-white-bokeh-background_1962-1324.jpg');">
        <div style="background-color: rgba(0, 0, 0, 0.6);">
            <div class="container mx-auto px-6 lg:px-20 py-12">
                <div class="lg:flex justify-center">
                    <div class="w-full lg:w-2/3">
                        <div class="lg:flex justify-center">
                            <div class="w-full mb-12 lg:mb-0 lg:w-1/2">
                                <h2 style="font-family: 'Baloo Tamma 2', cursive;"
                                    class="font-bold text-xl text-gray-100 mb-4">Hitta mig</h2>
                                 <div id="box" class="text-gray-500 m-1" style="cursor: pointer;" onclick="window.location='https://www.facebook.com/Gustav.Lofqvist';">
                                      <img width="50vw" src="ContactLogos/Facebooklogo.png">
                                      <span class="hover:text-red-300">&nbsp;&nbsp;Gustav&nbsp;Löfqvist</span>
                                    </div> 

                                    <div id="box" class="text-gray-500 m-1" style="cursor: pointer;" onclick="window.location='https://www.instagram.com/gustavlofqvist/';">
                                      <img width="50vw" src="ContactLogos/Instagramlogo.png">
                                      <span class="hover:text-red-300">&nbsp;&nbsp;Gustav&nbsp;Löfqvist</span>
                                    </div> 

                                    <div id="box" class="text-gray-500 m-1">
                                      <img width="50vw" src="ContactLogos/Snapchatlogo.png">
                                      <span class="hover:text-red-300" >&nbsp;&nbsp;Gustav.Lofqvist</span>
                                    </div> 
                            </div>
                            <div class="w-full lg:w-1/2 lg:flex lg:px-6 lg:justify-end">
                                <div class="w-full mb-6 lg:mb-0 lg:w-1/2 m-10">
                                    <h2 style="font-family: 'Baloo Tamma 2', cursive;" class="font-bold text-xl text-gray-100 mb-4">Länkar</h2>
                                  <ul class="text-gray-500 text-sm">
                                    <li class="pt-1 pb-2"><NuxtLink to="/simning" class="text-gray-500 text-sm hover:underline hover:text-red-300">Simning</NuxtLink></li>
                                    <li class="pt-1 pb-2"><NuxtLink to="/skola" class="text-gray-500 text-sm hover:underline hover:text-red-300">Skola</NuxtLink></li>
                                    <li class="pt-1 pb-2"><NuxtLink to="/fritid" class="text-gray-500 text-sm hover:underline hover:text-red-300">Fritid</NuxtLink></li>
                                  </ul>  
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
         <div style="font-family: 'Baloo Tamma 2', cursive; background-color: rgba(0, 0, 0, 0.7);">
                      <div class="container mx-auto px-6 lg:px-20 py-6">
                        <div class="flex font-light justify-center text-gray-500 text-sm">
                          <p>Designed by <span class="font-bold hover:text-red-300">Gustav Löfqvist</span></p>
                        </div>
                      </div>
                    </div>
                  </div>




  </div>
</template>

<style scoped>
#box {
   display: flex;
   align-items:center;
}


  #Header {    
    position: fixed;
    background: transparent;
    height: 72px;
    width: 100%;
    }

  #Header.fade-in { background: black;
                    box-shadow: 0px 0px 8px 1px #050505; 
                    width: 100%;
                  }
</style>

<script>
export default {
     data() {
       return {
         HeaderChecked: false
       }
    },

    mounted() {
      let recaptchaScript = document.createElement('script')
      recaptchaScript.setAttribute('src', 'https://www.google.com/recaptcha/api.js')
      document.head.appendChild(recaptchaScript)
      
    },

    created () {
      if (process.client) { 
          window.addEventListener('scroll', this.handleScroll);
      }
    },

    destroyed () {
      if (process.client) { 
          window.removeEventListener('scroll', this.handleScroll);
      }
    },

    methods: {
      toggle() {
        const open = document.getElementById("menu")
        const header = document.getElementById("Header")

        let scrollpos = window.scrollY

        open.classList.toggle("hidden")
        open.classList.toggle("bg-black")
      
        this.HeaderChecked = !this.HeaderChecked

        if (scrollpos == 0) {
        header.classList.toggle("fade-in") 
        }
      },

      handleScroll () {
        if (this.HeaderChecked) return;

        let scrollpos = window.scrollY

        const header = document.getElementById("Header")

        const add_class_on_scroll = () => header.classList.add("fade-in")
        const remove_class_on_scroll = () => header.classList.remove("fade-in")

        scrollpos = window.scrollY

        if (scrollpos >= 1) { add_class_on_scroll() }
        else { remove_class_on_scroll() }


      },

      closenav() {
        if (this.HeaderChecked) {
        const open = document.getElementById("menu")
        const header = document.getElementById("Header")

        let scrollpos = window.scrollY

        open.classList.toggle("hidden")
        open.classList.toggle("bg-black")
      
        this.HeaderChecked = !this.HeaderChecked

        if (scrollpos == 0) {
        header.classList.toggle("fade-in") 
        }
        }
      }
    },
}
</script>