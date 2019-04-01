<template>
  <div>
    <input type="text" :value="currentValue">
    <button @click="add">++</button>
    <button @click="redu">--</button>
  </div>
</template>

<script>
export default {
  name: 'Number',
  props: {
    value: {
      type: Number,
      default: 0
    },
    min: {
      type: Number,
      default: -Infinity
    },
    max: {
      type: Number,
      default: Infinity
    }
  },
  data: function () {
    return {
      currentValue: this.value
    }
  },
  methods: {
    add: function () {
      this.currentValue = this.currentValue++ < this.max ? this.currentValue : this.max;
    },
    redu: function () {
      this.currentValue = this.currentValue-- > this.min ? this.currentValue : this.min;
    }
  }
}
</script>

<style scoped>

</style>
