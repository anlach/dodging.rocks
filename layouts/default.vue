<template>
  <v-app dark>
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
            <v-icon v-if="item.icon !== ''">{{ item.icon }}</v-icon>
            <v-img v-else max-height="50" max-width="50" :src="item.img" />
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <!--src="https://anlach.github.io/images/assets/img/somerledi/IMG_20180410_140152091.jpg"-->
    <v-app-bar
      clipped-left
      fixed
      app
      src="~/assets/img/somerledi/IMG_20180410_140152091.jpg"
    >
      <template v-slot:img="{ props }">
        <v-img
          v-bind="props"
          gradient="to bottom, rgba(0,18,18,.9) 0%, rgba(18,18,18,0.4) 70%, rgba(15,15,15,1) 100%"
          position="30% 72.2%"
        ></v-img>
      </template>

      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      <v-toolbar-title v-text="title" />
      <v-spacer />
    </v-app-bar>
    <v-content>
      <v-container>
        <nuxt />
      </v-container>
    </v-content>
    <v-footer fixed app>
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      items: [
        {
          icon: 'mdi-buddhism',
          img: '',
          title: 'Home',
          to: '/'
        },
        {
          icon: '',
          img: '~/assets/somer.jpg',
          title: 'Somerledi',
          to: '/somerledi'
        },
        {
          icon: '',
          img: '~/assets/dink.jpg',
          title: 'Urist',
          to: '/dinghy'
        },
        {
          icon: '',
          img: '~/assets/rock-dodge.png',
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
