<template>
  <v-app dark>
    <v-content>
      <v-speed-dial
        v-model="drawer"
        absolute
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
          align="center"
          height="60px"
          width="220px"
          overflow="hidden"
          overflow-y="hidden"
          rounded
          color="green"
        >
          <img height="72" width="72" :src="item.img" />
          <p class="font-weight-bold text-uppercase">{{ item.title }}</p>
        </v-btn>
      </v-speed-dial>
    </v-content>
    <!-- <v-card id="create">
      <v-container fluid>
        <v-row class="child-flex">
          <v-col cols="12" sm="6" md="4">
            <v-subheader>Options</v-subheader>
            <v-checkbox
              v-model="hover"
              label="Open on hover"
              hide-details
            ></v-checkbox>
          </v-col>
          <v-col cols="12" sm="6" md="4">
            <v-subheader>FAB location</v-subheader>
            <v-checkbox v-model="top" label="Top" hide-details></v-checkbox>
            <v-checkbox v-model="right" label="Right" hide-details></v-checkbox>
            <v-checkbox
              v-model="bottom"
              label="Bottom"
              hide-details
            ></v-checkbox>
            <v-checkbox v-model="left" label="Left" hide-details></v-checkbox>
          </v-col>
          <v-col cols="12" sm="6" md="4">
            <v-subheader>Speed dial direction</v-subheader>
            <v-radio-group v-model="direction" hide-details>
              <v-radio value="top" label="Top"></v-radio>
              <v-radio value="right" label="Right"></v-radio>
              <v-radio value="bottom" label="Bottom"></v-radio>
              <v-radio value="left" label="Left"></v-radio>
            </v-radio-group>
          </v-col>
          <v-col cols="12" sm="6" md="4">
            <v-subheader>Transition</v-subheader>
            <v-radio-group v-model="transition" hide-details>
              <v-radio value="slide-y-transition" label="Slide y"></v-radio>
              <v-radio
                value="slide-y-reverse-transition"
                label="Slide y reverse"
              ></v-radio>
              <v-radio value="slide-x-transition" label="Slide x"></v-radio>
              <v-radio
                value="slide-x-reverse-transition"
                label="Slide x reverse"
              ></v-radio>
              <v-radio value="scale-transition" label="Scale"></v-radio>
            </v-radio-group>
          </v-col>
        </v-row>
      </v-container>
      <v-speed-dial
        v-model="fab"
        :top="top"
        :bottom="bottom"
        :right="right"
        :left="left"
        :direction="direction"
        :open-on-hover="hover"
        :transition="transition"
      >
        <template v-slot:activator>
          <v-btn v-model="fab" color="blue darken-2" dark fab>
            <v-icon v-if="fab">mdi-close</v-icon>
            <v-icon v-else>mdi-account-circle</v-icon>
          </v-btn>
        </template>
        <v-btn fab dark small color="green">
          <v-icon>mdi-pencil</v-icon>
        </v-btn>
        <v-btn fab dark small color="indigo">
          <v-icon>mdi-plus</v-icon>
        </v-btn>
        <v-btn fab dark small color="red">
          <v-icon>mdi-delete</v-icon>
        </v-btn>
      </v-speed-dial>
    </v-card> -->
    <!-- <v-menu v-model="drawer" absolute>
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
    </v-menu> -->

    <v-content>
      <v-container>
        <!-- <nuxt /> -->
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
