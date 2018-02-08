<template>
  <div class="numberItem">
    <div class="item">
      <h1>Trivi#:</h1><span><p>{{trivia}}</p></span>
    </div>
    <div class="item">
      <h1>Ye#r:</h1><span><p>{{year}}</p></span>
    </div>
    <div class="item">
      <h1>M#th:</h1><span><p>{{math}}</p></span>
    </div>
    <div class="item">
      <h1>D#te:</h1><span><p>{{date}}</p></span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'NumberItem',
  props: ['trivia', 'year', 'math', 'date'],
  data() {
    return {
      msg: '#########'
    };
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
h1,
h2 {
  font-weight: normal;
}
.numberItem {
  padding: 5rem 2rem;
}
.item {
  display: flex;
  align-items: baseline;
  justify-content: center;
  line-height: 5rem;
  flex-wrap: wrap;
}
p {
  padding-left: 2rem;
}
</style>
