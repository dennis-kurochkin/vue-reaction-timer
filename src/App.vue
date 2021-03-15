<template>
  <h1>Reaction Timer Game</h1>

  <button type="button"
          @click="start"
          :disabled="isPlaying"
  >
    Play!
  </button>

  <Block v-if="isPlaying"
         :delay="delay"
         @click="boxClickHandler"
  />

  <Results v-if="isFinished" />
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
  data() {
    return {
      isPlaying: false,
      isFinished: false,
      delay: null,
    }
  },
  methods: {
    start() {
      this.delay = 1000 + Math.floor(Math.random() * 2000);
      this.isPlaying = true;
      this.isFinished = false;
    },
    boxClickHandler() {
      this.isPlaying = false;
      this.isFinished = true;
    },
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
