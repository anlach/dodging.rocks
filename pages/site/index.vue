<template>
  <v-layout column justify-center align-center>
    <v-flex xs12 sm8 md6>
      <div class="text-center">
        <logo />
        <vuetify-logo />
      </div>
      <v-card>
        <v-card-title class="headline">
          This site was built by Andew LaCharite using Vue.js with Nuxt.js and
          Vuetify.js.
        </v-card-title>
        <v-card-text>
          <a href="https://vuetifyjs.com" target="_blank">
            Vuetify documentation
          </a>
          <br />

          <a href="https://nuxtjs.org/" target="_blank">
            Nuxt Documentation
          </a>
        </v-card-text>
        <v-card-actions>
          <v-spacer />
          <v-btn color="primary" nuxt to="/inspire">
            Continue
          </v-btn>
        </v-card-actions>
      </v-card>
    </v-flex>
  </v-layout>
</template>

<script>
import Logo from '~/components/Logo.vue'
import VuetifyLogo from '~/components/VuetifyLogo.vue'

export default {
  components: {
    Logo,
    VuetifyLogo
  }
}
</script>

<style lang="scss" scoped></style>
