<template>
  <div class="criteria-group">
    <select v-model="count">
      <option v-for="n in countSelectItems" v-text="n" :key="n"></option>
    </select>
    <div>
      <input v-for="n in Number(count)" :key="n" v-model="values[n]">
    </div>
  </div>
</template>

<script>
export default {
  name: 'CriteriaInput',
  props: {
    minCount: {
      type: Number,
      default: 2
    },
    maxCount: {
      type: Number,
      default: 7
    }
  },
  data: function () {
    return {
      count: 2,
      values: []
    }
  },
  computed: {
    countSelectItems: function () {
      return Array.from(Array(this.maxCount - this.minCount + 1), (x, i) => i + this.minCount)
    }
  }
}
</script>

<style scoped>
/* Styles goes here */
input {
  display: block;
  margin: 1em;
}
</style>
