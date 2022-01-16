<template>
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

    <v-btn
      class="mr-4"
    >
      submit
    </v-btn>
    <v-btn @click="clear">
      clear
    </v-btn>
  </form>
</template>
<script>

export default {
  name: 'OrganisationAdd',
  data: () => ({
    name: '',
    email: '',
    select: null,
    items: [
      'Item 1',
      'Item 2',
      'Item 3',
      'Item 4'
    ],
    checkbox: false
  })
}
</script>

<style scoped>

</style>
