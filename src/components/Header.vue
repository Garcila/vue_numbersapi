<template>
  <div class="header">
    <div class="number">#</div>
    <h1>{{ msg }}</h1>
  </div>
</template>

<script>
export default {
  name: 'Header',
  data() {
    return {
      msg: 'There is a # for that'
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

.header {
  background-size: cover;
  background-position: top;
  background-image: linear-gradient(
      to right bottom,
      rgba(150, 175, 177, 0.2),
      rgba(77, 187, 199, 0.2)
    ),
    url('https://res.cloudinary.com/garcila/image/upload/c_scale,q_auto:good,w_1667/v1517886293/chris-barbalis-152597_evyhth.png');
  padding: 2rem;
}

.number {
  color: rgba(255, 255, 255, 0.8);
  font-size: 19rem;
  height: 25vh;
}
h1 {
  font-size: 4rem;
  color: rgba(255, 255, 255, 1);
}
</style>
