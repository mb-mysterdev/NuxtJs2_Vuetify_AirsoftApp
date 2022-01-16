<template>
  <div class="text-center">
    <v-dialog
      :value="dialog"
      width="500"
    >
      <v-card>
        <form>
          <v-text-field
            v-model="name"
            :counter="10"
            label="Name"
            required
          />
          <v-text-field
            v-model="email"
            label="E-mail"
            required
          />
          <v-select
            v-model="select"
            :items="items"
            label="Item"
            required
          />
          <v-checkbox
            v-model="checkbox"
            label="Do you agree?"
            required
          />

          <v-btn @click="$emit('dialogPartie',false)">
            OK
          </v-btn>
        </form>
      </v-card>
    </v-dialog>
  </div>
</template>

<script>
export default {
  name: 'PartieSubscriber',
  props: {
    dialog: {
      type: Boolean,
      default: false
    }
  }
}
</script>

<style scoped>

</style>
