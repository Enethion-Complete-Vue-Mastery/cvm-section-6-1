<template>
  <p v-if="age >= 25" v-text="msg" />
  <p v-else>You're way to loung...</p>
</template>

<script>
export default {
  name: "Greeting",
  props: ['age'],
  data() {
    return {
      msg: "Hello world!"
    }
  },
}
</script>

<style scoped lang="scss">
$color: red;
p {
  color: $color;
}
</style>