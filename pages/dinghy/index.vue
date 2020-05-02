<template>
  <v-carousel height="100vh" show-arrows-on-hover>
    <v-carousel-item
      v-for="(src, i) in filenames"
      :key="i"
      :src="'/img/dinghy/' + src"
    >
    </v-carousel-item>
  </v-carousel>
</template>

<script>
export default {
  data() {
    return {
      filenames: [
        'pram-panel-2.jpg',
        'pram-ends-1.jpg',
        'epoxy-bulkhead-1.jpg',
        'pram-panel-3.jpg',
        'pram-stitched-1.jpg',
        'pram-stitched-2.jpg',
        'pram-port-gunnel-1.jpg',
        'pram-starboard-gunnel-1.jpg',
        'pram-stern-knees-1.jpg',
        'pram-bow-knees-1.jpg',
        'pram-thwarts-1.jpg',
        'pram-epoxy-1.jpg',
        'thwart-supports-1.jpg',
        'pram-bottom-epoxy-1.jpg',
        'pram-cut-1.jpg',
        'nesting-pram-1.jpg',
        'bottom-sanded-1.jpg',
        'bottom-painted-1.jpg',
        'varnished-1.jpg',
        'pre-splash-1.jpg',
        'stowed-1.jpg',
        'cartopped-1.jpg',
        'north-shore-1.jpg'
      ]
    }
  }
}
</script>

<style lang="scss" scoped></style>
