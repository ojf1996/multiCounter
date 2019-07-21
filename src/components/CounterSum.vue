<template>
  <span>{{ sum }}</span>
</template>

<script>
export default {
  name: "counterSum",
  props: {
    sum: {
      type: Number,
      default: 0
    }
  }
}
</script>

<style>
</style>
