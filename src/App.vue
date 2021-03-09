<template>
  <Block />
  <Results />
</template>

<script>
import Block from './components/Block';
import Results from './components/Results';

export default {
  name: 'App',
  components: {
    Block,
    Results,
  },
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #444444;
  margin-top: 60px;
}
</style>
