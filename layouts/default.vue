<template>
  <v-app dark>
    <v-app-bar
      :clipped-left="clipped"
      app
      fixed
    >
      <div class="d-flex justify-center" style="margin-left: 11rem">
        <v-btn>LOGO</v-btn>
        <div style="margin-left: 3rem">
          <v-btn class="mr-5" @click="$router.push('/')">
            Accueil
          </v-btn>
          <v-btn class="mr-5" @click="$router.push('/parties')">
            Parties
          </v-btn>
          <v-btn class="mr-5" @click="$router.push('/organisations')">
            Organisations
          </v-btn>
          <v-btn class="mr-5" @click="$router.push('/equipes')">
            Les équipes
          </v-btn>
        </div>
      </div>
      <v-spacer />
      <v-btn class="mr-5" @click="$router.push('/connexion')">
        Connexion
      </v-btn>
    </v-app-bar>
    <v-main>
      <Nuxt />
    </v-main>
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
