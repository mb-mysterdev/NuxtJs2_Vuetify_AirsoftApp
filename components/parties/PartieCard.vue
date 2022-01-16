<template>
  <div>
    <partie-subscriber :dialog="dialog" @dialogPartie="dialog = $event" />
    <v-card
      :loading="loading"
      class="mx-auto my-12"
      max-width="374"
    >
      <template slot="progress">
        <v-progress-linear
          color="deep-purple"
          height="10"
          indeterminate
        />
      </template>

      <v-img
        height="250"
        src="https://lvdneng.rosselcdn.net/sites/default/files/dpistyles_v2/ena_16_9_extra_big/2020/08/28/node_857044/48789474/public/2020/08/28/B9724377493Z.1_20200828113816_000%2BG7TGHUJ1I.2-0.jpg?itok=r962Z5Ib1598607513"
      />

      <v-card-title>Debarquement de Normandie</v-card-title>

      <v-card-text>
        <div>Small plates, salads & sandwiches - an intimate setting with 12 indoor seats plus patio seating.</div>
      </v-card-text>

      <v-divider class="mx-4" />

      <v-card-title>Heures de la partie</v-card-title>

      <v-card-text>
        <v-chip-group
          v-model="selection"
          active-class="deep-purple accent-4 white--text"
          column
        >
          <v-chip>9:30PM</v-chip>

          <v-chip>18:00PM</v-chip>
        </v-chip-group>
      </v-card-text>

      <v-card-actions>
        <div class="d-flex justify-space-between">
          <v-btn
            color="deep-purple lighten-2"
            text
            @click="dialog = true"
          >
            S'inscrire
          </v-btn>
          <v-btn
            color="deep-purple lighten-2"
            text
            @click="$router.push('/parties/1')"
          >
            Voir plus
          </v-btn>
        </div>
      </v-card-actions>
    </v-card>
  </div>
</template>

<script>
import PartieSubscriber from '~/components/parties/PartieSubscriber'

export default {
  name: 'PartieCard',
  components: { PartieSubscriber },
  data () {
    return {
      dialog: false
    }
  }
}
</script>

<style scoped>

</style>
