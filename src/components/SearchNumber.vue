<template>
  <div class="SearchNumber">
    <input @keyup.enter="goAndSearch" type="text" v-model="desiredNumber" placeholder="Enter a number, year or date">
  </div>
</template>

<script>
export default {
  name: 'SearchNumber',
  data() {
    return {
      desiredNumber: ''
    };
  },
  methods: {
    goAndSearch () {
      this.$emit('goSearch', this.desiredNumber)
      this.desiredNumber = ''
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
*,
*::after,
*::before {
  margin: 0;
  padding: 0;
  box-sizing: inherit;
}

</style>
