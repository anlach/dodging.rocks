<template>
  <v-app dark>
    <v-app-bar
      clipped-left
      hide-on-scroll
      fixed
      app
      src="/img/somerledi/IMG_20180410_140152091.jpg"
    >
      <template v-slot:img="{ props }">
        <v-img
          v-bind="props"
          gradient="to right, rgba(0, 50, 50,.65) 0%, rgba(0,18,18,.75) 100%"
          position="30% 72.2%"
        ></v-img>
      </template>

      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      <v-spacer />
    </v-app-bar>
    <v-navigation-drawer v-model="drawer" clipped app>
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-item-action>
            <div v-if="item.icon !== ''">
              <v-icon x-large>{{ item.icon }}</v-icon>
            </div>
            <v-img v-else height="72" width="72" :src="item.img" />
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

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
  data() {
    return {
      items: [
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
      title: 'Dodging Rocks'
    }
  }
}
</script>
