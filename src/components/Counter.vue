<template>
  <div class="hello">
    <button @click="decrease">
      -
    </button>
    <span>
      {{ count }}
    </span>
    <button @click="increase">
      +
    </button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data() {
    return {
      count: 0
    }
  },
  methods: {
    increase() {
      this.count++
      this.$emit("update:sum", this.count)
    },
    decrease() {
      this.count--
      this.$emit("update:sum", this.count)
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.hello {
  width: 100px;
  height: 30px;;
}
</style>
