<template>
  <div id="app">
    <CounterGroup/>
  </div>
</template>

<script>
import CounterGroup from '@/components/CounterGroup'

export default {
  name: 'app',
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
