<template>
  <div id="app">
    <NumberInput v-model="value" :max="10" :min="1"></NumberInput>
  </div>
</template>

<script>
import NumberInput from './components/Number'
export default {
  name: 'App',
  components: {
    NumberInput
  },
  data: function () {
    return {
      value: 5
    }
  },
  methods: {

  }
}
</script>
