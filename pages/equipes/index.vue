<template>
  <div>
    <v-container>
      <h1 class="d-flex justify-center">
        Toutes les teams
      </h1>

      <v-row>
        <v-col
          v-for="item in 12"
          :key="item"
          cols="4"
        >
          <team-card />
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
import TeamCard from '~/components/teams/TeamCard'

export default {
  name: 'Index',
  components: {
    TeamCard
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
