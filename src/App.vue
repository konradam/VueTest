<template>
  <v-app>
    <v-title>{{msg}}</v-title>
    <h1>{{age}}</h1>
    <control></control>
    <keyboard></keyboard>
  </v-app>
</template>

<script>
import Hello from './components/HelloWorld.vue'
import Keyboard from './components/Keyboard.vue'

export default {
  props: {
    age: {
      type: Number,
      default: 20
    }
  },
  components: {
    'control': Hello,
    'keyboard': Keyboard
  },
  data () {
    return {
      msg: "Hello world :)"
    }
  },
  methods: {
    greeting: function(){
      return "Greeting from function"
    }
  }
}
</script>