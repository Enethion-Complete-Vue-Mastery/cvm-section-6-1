<template>
  <p>The user is {{age}} years young</p>
  <p>Double it will be {{ageDoubled}}</p>
  <button @click="onClickAge">Add a year</button>
  <button @click="cbFn(53)">Add a year, but with callback</button>
</template>

<script>
export default {
  name: "User",
  props: {
    age: {
      type: Number,
      // required: true
      // default: 20,
      validator(value) {
        return value > 0 && value < 130
      }
    },
    cbFn: {
      
    }
  },
  methods: {
    onClickAge() {
      this.$emit('updateAge', 3) 
    }
  },
  computed: {
    ageDoubled() {
      return this.age * 2
    }
  },
  emits: ['updateAge']
};
</script>