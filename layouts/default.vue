<template>
  <v-app>
    <v-app-bar
      v-scroll="onScroll"
      :color="!isScrolling ? 'transparent' : 'white'"
      fixed
      flat
    >
    <!-- <v-slide-x-transition> -->
      <!-- <v-img
        v-if="showLogo"
        class="shrink"
        contain
        height="50"
      >
      Portfolio Website
      </v-img> -->
    <!-- </v-slide-x-transition> -->
    <v-spacer />
    <social-media />

    </v-app-bar>
    <v-main class="gradient-bg">
      <v-container>
        <Nuxt/>
      </v-container>
    </v-main>
  
  <v-footer
    :absolute="!fixed"
    app
    height="70"
    class="justify-center"
  >
    <social-media large/>
  </v-footer>
  </v-app>
</template>

<script>
export default {
  data () {
  return {
    clipped: false,
    drawer: false,
    fixed: false,
    showLogo: true,
    isScrolling: false,
    items: [
    {
      icon: 'mdi-apps',
      title: 'Welcome',
      to: '/'
    },
    ],
    right: true,
    title: 'Vuetify.js'
  }
  },
  methods: {
    onScroll () {
    const offset = window.pageYOffset
    this.isScrolling = offset > 50
    this.showLogo = offset > 200
    },
  },
}
</script>

<style>
.gradient-bottom{
  background-image: linear-gradient(to bottom, #cacaca, white);
}
.gradient-top{
  background-image: linear-gradient(to top, #E2EBF1, white);
}
.gradient-bg{
  background-image: linear-gradient(to top, #f5f5f5, white);
}
</style>