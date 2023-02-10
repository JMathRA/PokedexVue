<template>
  <v-app>
    <v-main>
      <v-container>
        <router-view />
      </v-container>
      <Scrolltotop />
    </v-main>
  </v-app>
</template>

<script>
import Scrolltotop from "@/components/Scrolltotop.vue";

export default {
  name: 'App',
  data: () => ({
    //
  }),
  components: {
    Scrolltotop
  },
  metaInfo() {
    return { 
        title: "Pokédex - a web and pwa compatible",
        meta: [
            { name: 'description', content:  'A Simple Web App and PWA compatible Pokédex built with VueJS and data was based on https://pokeapi.co/ Build for the pokemon lover and enthusiast. Made with dedication by João Matheus'},
            { property: 'og:title', content: "Pokédex - a web and pwa compatible"},
            { property: 'og:site_name', content: 'Pokédex'},
            { property: 'og:type', content: 'website'},    
            { name: 'robots', content: 'index,follow'} 
        ]
    }
  }
};
</script>
