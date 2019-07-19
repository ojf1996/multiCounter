<template>
  <div class="group">
    <div v-for="n in counterNumber" :key="n">
      <Counter/>
    </div>
  </div>
</template>

<script>
import Counter from "@/components/Counter"

export default {
  name: "CounterGroup",
  components: { Counter },
  data() {
    return {
      counterNumber: 3
    }
  }
}
</script>

<style>
.group {
  width: inherit;
  height: inherit;
}
</style>