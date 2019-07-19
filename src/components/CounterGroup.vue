<template>
  <div class="group">
    <Counter/>
  </div>
</template>

<script>
import Counter from "@/components/Counter"

export default {
  name: "CounterGroup",
  components: { Counter },
  data() {
    return {
      counterNumber: 1
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