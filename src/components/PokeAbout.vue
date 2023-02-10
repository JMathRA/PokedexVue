<template>
  <v-dialog
    max-width="400"
    content-class="about__dialog"
    v-model="dialog"
    transition="fade-transition"
  >
    <v-card class="pokemon__card">
      <v-card-title>
        About
        <v-spacer></v-spacer>
        <v-btn icon @click="dialog = false" class="mdl__close">
          <v-icon>mdi-close</v-icon>
        </v-btn>
      </v-card-title>
      <v-card-text class="about__container">
        <v-container>
            <div class="justify-center align-center">
                <p class="headline text-h5 text-capitalize font-weight-black">Pokédex</p>
                <div class="about__content">
                    <p>
                      Project made as a challenge for the Copybase frontend developer vacancy
                    </p>
                    <p>
                    Built with <a :href="vuejs" target="_blank">Vue JS</a>,
                    <a :href="vuetify" target="_blank">Vuetify</a>, and
                    <a :href="pokeapi" target="_blank">PokéAPI</a>.
                    </p>
                    <p>
                    Special Thanks to <a :href="pokemon" target="_blank">Pokémon</a>, the
                    original website.
                    </p>
                    
                </div>
                <div class="about__footer">
                    <p class="text-caption text-center"><strong> Made with dedication by <a :href="website" target="_blank">João Matheus</a>.</strong></p>
                </div>
            </div>
        </v-container>
      </v-card-text>
    </v-card>
  </v-dialog>
</template>

<script>
export default {
  name: "PokédexAbout",
  data: () => ({
      dialog: false,
      vuejs: "https://vuejs.org/",
      vuetify: "https://vuetifyjs.com",
      pokeapi: "https://pokeapi.co/",
      pokemon: "https://www.pokemon.com/us/",
      github: "https://github.com/JMathRA",
      website: "https://www.linkedin.com/in/jo%C3%A3o-matheus-ribeiro-albuquerque-830a81207/",
  }),
  methods: {
    about() {
        this.dialog = true;
    }
  }
};
</script>