<template>
  <v-app dark>
    <v-app-bar
      :clipped-left="clipped"
      fixed
      app
    >
      <div style="margin-left: 11rem" class="d-flex justify-center">
        <v-btn>LOGO</v-btn>
        <div style="margin-left: 3rem">
          <v-btn class="mr-5">
            Accueil
          </v-btn>
          <v-btn class="mr-5">
            Parties
          </v-btn>
          <v-btn class="mr-5">
            Organisations
          </v-btn>
        </div>
      </div>
    </v-app-bar>
    <v-main>
      <Nuxt />
    </v-main>
    <v-footer
      :absolute="!fixed"
      app
    >
      <span>&copy; {{ new Date().getFullYear() }}</span>
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
      items: [
        {
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Inspire',
          to: '/inspire'
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js'
    }
  }
}
</script>
