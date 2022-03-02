<template>
  <p>Hey!</p>
  <greeting :age="age" />
  <user :age="age" @updateAge="onUpdateAge" :cbFn="cbAgeUpdate"/>
</template>

<script>
import Greeting from './components/Greeting.vue'
import User from './components/User.vue'
export default {
  components: { Greeting, User },
  name: 'App',
  data() {
    return {
      age: 20
    }
  },
  methods: {
    onUpdateAge(value){
      this.age += value
    },
    cbAgeUpdate(value){
      this.age += value
    }
  }
}
</script>
