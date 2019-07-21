<template>
  <div class="group">
    <div v-for="n in counterNumber" :key="n">
      <Counter v-on:update:sum="updataSum(n, $event)"/>
    </div>
    <CounterSum :sum="sumOfAllCounter"/>
  </div>
</template>

<script>
import Counter from "@/components/Counter"
import CounterSum from '@/components/CounterSum'
import { constants } from 'crypto';

export default {
  name: "CounterGroup",
  components: { Counter, CounterSum },
  props: {
    counterNumber: {
      type: Number,
      default: 1
    }
  },
  data() {
    return {
      sum : []
    }
  },
  watch: {
    counterNumber(newValue, oldValue) {
      console.log(oldValue, newValue)
      const numChaged = Math.abs(oldValue - newValue)
      for (let i = 0; i < numChaged; ++i) {
        if (oldValue - newValue > 0) {
          this.sum.splice(this.sum.length - 1, 1)
        } else if (oldValue - newValue < 0) {
          this.sum.splice(this.sum.length, 0, 0)
        }
      }
    }
  },
  computed: {
    sumOfAllCounter() {
      console.log(this.sum)
      let num = this.sum.reduce((acc,num) => { return acc + num }, 0)
      return num
    }
  },
  methods: {
    updataSum(index, num) {
      this.$set(this.sum, index, num)
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