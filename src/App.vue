<template>
  <div id="app">
    <input v-model="counterNumber"/>
    <CounterGroup :counterNumber="parseInt(counterNumber) || 0"/>
  </div>
</template>

<script>
import CounterGroup from '@/components/CounterGroup'

export default {
  name: 'app',
  data() {
    return {
      counterNumber: 0
    }
  },
  components: {
    CounterGroup
  }
}
</script>

<style>
#app {
  width: 100%;
  height: 100%;
  display: block;
}
html,body {
  width: 100%;
  height: 100%;
}
</style>
