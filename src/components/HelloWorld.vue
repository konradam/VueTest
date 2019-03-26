<template>
  <div>
    <h2>{{info}}</h2>
    <v-btn dark v-on:click="add()">Increase age</v-btn>
    <v-btn round v-on:click="substract(5)">Decrease age</v-btn>
    <h5>{{age}}</h5>
  </div>
</template>

<script>
export default {
  props: {
    age: {
      type: Number,
      default: 20
    }
  },
  data () {
    return {
      info: 'Nested component'
    }
  },
  methods: {
    add: function(inc = 1){
      this.age += inc;
    },
    substract: function(dec){
      this.age -=dec;
    }
  }
}
</script>

<style>

</style>
