<template>
  <div>
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
        src="https://lvdneng.rosselcdn.net/sites/default/files/dpistyles_v2/ena_16_9_extra_big/2020/09/24/node_869694/49073910/public/2020/09/24/B9724678734Z.1_20200924102506_000%2BG67GNLI5B.2-0.jpg?itok=du5lymEb1600935913"
      />

      <v-card-title>Airsoft les lions</v-card-title>

      <v-card-text>
        <div>Small plates, salads & sandwiches - an intimate setting with 12 indoor seats plus patio seating.</div>
      </v-card-text>

      <v-divider class="mx-4" />

      <v-card-actions>
        <div class="d-flex justify-space-between">
          <v-btn
            color="deep-purple lighten-2"
            text
            @click="$router.push('/organisations/1')"
          >
            Voir plus
          </v-btn>
        </div>
      </v-card-actions>
    </v-card>
  </div>
</template>

<script>
export default {
  name: 'OrganisationCard'
}
</script>

<style scoped>

</style>
