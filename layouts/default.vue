<template>
  <v-app dark>
    <v-content>
      <v-speed-dial
        v-model="drawer"
        fixed
        top
        left
        direction="bottom"
        transition="slide-y-transition"
      >
        <template v-slot:activator>
          <v-btn v-model="drawer" x-large dark fab>
            <v-icon v-if="drawer" x-large>mdi-close</v-icon>
            <v-icon v-else x-large>mdi-buddhism </v-icon>
          </v-btn>
        </template>
        <v-btn
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          fab
          router
          x-large
          height="60px"
          width="210px"
          rounded
        >
          <v-row no-gutters>
            <v-col cols="4">
              <v-avatar size="56">
                <img :src="item.img" />
              </v-avatar>
            </v-col>
            <v-col cols="8" style="align-self: center">
              {{ item.title }}
            </v-col>
          </v-row>
        </v-btn>
      </v-speed-dial>
    </v-content>

    <v-content>
      <v-container>
        <nuxt />
      </v-container>
    </v-content>
  </v-app>
</template>

<script>
// const test = require('~/assets/dink.jpg')

// console.log('here it is:', test)
export default {
  data: () => {
    return {
      items: [
        {
          icon: '',
          img: '/img/somerledi/sunset1.jpg',
          title: 'Home',
          to: '/'
        },
        {
          icon: '',
          img: '/somer.jpg',
          title: 'Somerledi',
          to: '/somerledi'
        },
        {
          icon: '',
          img: '/dink.jpg',
          title: 'Urist',
          to: '/dinghy'
        },
        {
          icon: '',
          img: '/rock-dodge.png',
          title: 'Site',
          to: '/site'
        }
      ],
      drawer: false,
      title: 'Dodging Rocks',

      direction: 'top',
      fab: false,
      fling: false,
      hover: false,
      tabs: null,
      top: false,
      right: true,
      bottom: true,
      left: false,
      transition: 'slide-y-reverse-transition'
    }
  },
  computed: {
    activeFab() {
      switch (this.tabs) {
        case 'one':
          return { class: 'purple', icon: 'account_circle' }
        case 'two':
          return { class: 'red', icon: 'edit' }
        case 'three':
          return { class: 'green', icon: 'keyboard_arrow_up' }
        default:
          return {}
      }
    }
  }
}
</script>

<style>
.v-speed-dial--direction-bottom .v-speed-dial__list {
  left: 0;
  width: 300px;
}
</style>
