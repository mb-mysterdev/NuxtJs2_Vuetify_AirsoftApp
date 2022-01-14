<template>
  <div>
    <v-container>
      <h1 class="d-flex justify-center">
        Toutes les organisations
      </h1>

      <v-row>
        <v-col
          v-for="item in 12"
          :key="item"
          cols="4"
        >
          <organisation-card />
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
import OrganisationCard from '~/components/organisations/OrganisationCard'

export default {
  name: 'Index',
  components: {
    OrganisationCard
  },
  data () {
    return {
      dialog: false,
      colors: [
        'indigo',
        'warning',
        'pink darken-2',
        'red lighten-1',
        'deep-purple accent-4'
      ],
      slides: [
        'First',
        'Second',
        'Third',
        'Fourth',
        'Fifth'
      ]
    }
  }
}
</script>
