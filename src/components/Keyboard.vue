<template>
  <div>
    <h2>Keyboard</h2>
    <v-text-field label="Name" outline style="width: 10cm"/>
    <h2>{{lastname}}</h2>
  </div>
</template>

<script>
export default {
  props: {
    name: {
      type: String
    },
    lastname: {
      type: String
    },
    email: {
      type: String
    }
  },
  methods: {

  }
}
</script>

<style scoped>
.input-name {
    width: 10cm;
}

</style>