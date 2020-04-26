<template>
  <v-content>
    <section id="quote">
      <v-row no-gutters>
        <v-img
          :min-height="'calc(100vh - ' + $vuetify.application.top + 'px)'"
          src="/img/somerledi/sunset1.jpg"
        >
          <v-theme-provider dark>
            <v-container fill-height>
              <v-row align="center" class="mx-auto" justify="center">
                <v-col
                  class="text-center text-uppercase"
                  cols="12"
                  tag="h3"
                  style="font-family: 'Gaegu';font-size: 45px;"
                >
                  Happiness Only Real When Shared
                </v-col>

                <v-col class="white--text text-center" cols="12">
                  -Christopher McCandless
                </v-col>

                <v-btn
                  class="align-self-end"
                  fab
                  outlined
                  @click="$vuetify.goTo('#about-me')"
                >
                  <v-icon>mdi-chevron-double-down</v-icon>
                </v-btn>
              </v-row>
            </v-container>
          </v-theme-provider>
        </v-img>
      </v-row>
    </section>

    <section id="about-me">
      <div class="py-12"></div>

      <v-container class="text-center">
        <h2 class="display-2 font-weight-bold mb-3">WHO AM I?</h2>

        <v-responsive class="mx-auto mb-8" width="56">
          <v-divider class="mb-1"></v-divider>

          <v-divider></v-divider>
        </v-responsive>

        <v-responsive
          class="mx-auto title font-weight-light mb-8"
          max-width="720"
        >
          Maybe I'll put one of those word collages here...
        </v-responsive>

        <v-avatar class="elevation-12 mb-12" size="128">
          <v-img src="/img/me/library-boat.jpg"></v-img>
        </v-avatar>
      </v-container>

      <div class="py-12"></div>
    </section>
  </v-content>
</template>

<script>
export default {}
</script>

<style>
/* .v-parallax__image {
  left: 100%;
} */
</style>
