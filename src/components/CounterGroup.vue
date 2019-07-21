<template>
  <div class="group">
    <div v-for="n in counterNumber" :key="n">
      <Counter/>
    </div>
    <CounterSum :sum="0"/>
  </div>
</template>

<script>
import Counter from "@/components/Counter"
import CounterSum from '@/components/CounterSum'

export default {
  name: "CounterGroup",
  components: { Counter, CounterSum },
  props: {
    counterNumber: {
      type: Number,
      default: 1
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