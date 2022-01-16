<template>
  <v-row>
    <v-col
      v-for="item in 4"
      :key="item"
      cols="4"
    >
      <partie-card />
    </v-col>
  </v-row>
</template>

<script>
import PartieCard from '~/components/parties/PartieCard'

export default {
  name: 'OrganisationContentParties',
  components: { PartieCard }
}
</script>

<style scoped>
.d-grid {
  display: grid;
}
</style>
