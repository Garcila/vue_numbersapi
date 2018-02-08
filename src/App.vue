<template>
  <div id="app">
    <Header/>
    <SearchNumber @goSearch="goSearch"/>
    <NumberItem :trivia="trivia" :year="year" :math="math" :date="date"/>
  </div>
</template>

<script>
import axios from 'axios';
import NumberItem from './components/NumberItem';
import Header from './components/Header';
import SearchNumber from './components/SearchNumber';

export default {
  name: 'App',
  components: {
    Header,
    NumberItem,
    SearchNumber,
  },
  data() {
    return {
      trivia: '',
      math: '',
      year: '',
      date: '',
    };
  },
  mounted() {
    axios
      .get('http://numbersapi.com/42/trivia')
      .then(response => (this.trivia = response.data));
    axios
      .get('http://numbersapi.com/42/year')
      .then(response => (this.year = response.data));
    axios
      .get('http://numbersapi.com/42/math')
      .then(response => (this.math = response.data));
    axios
      .get('http://numbersapi.com/42/date')
      .then(response => (this.date = response.data));
  },
  methods: {
    goSearch(e) {
    axios
      .get(`http://numbersapi.com/${e}/trivia`)
      .then(response => (this.trivia = response.data));
    axios
      .get(`http://numbersapi.com/${e}/year`)
      .then(response => (this.year = response.data));
    axios
      .get(`http://numbersapi.com/${e}/math`)
      .then(response => (this.math = response.data));
    axios
      .get(`http://numbersapi.com/${e}/date`)
      .then(response => (this.date = response.data));
    },
  },
};
</script>

<style>
*,
*::after,
*::before {
  margin: 0;
  padding: 0;
  box-sizing: inherit; }
#app {
  font-family: 'Special Elite', cursive, 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
</style>
