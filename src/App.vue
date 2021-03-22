<template>
    <h1>Reaction Timer Game</h1>
    <button type="button"
            :disabled="isPlaying"
            @click="start"
    >
        Play!
    </button>
    <Block v-if="isPlaying"
          :delay="delay"
          @end="boxEndHandler"
    />
    <Results v-if="isFinished"
             :score="score"
    />
</template>

<script>
import Block from '@/components/Block';
import Results from '@/components/Results';

export default {
    name: 'App',
    components: {
        Block,
        Results,
    },
    data() {
        return {
            delay: null,
            score: null,
            isPlaying: false,
            isFinished: false,
        };
    },
    methods: {
        start() {
            this.delay = 1000 + Math.floor(Math.random() * 2000);
            this.isPlaying = true;
            this.isFinished = false;
        },
        boxEndHandler(reactionTime) {
            this.score = reactionTime;
            this.isPlaying = false;
            this.isFinished = true;
        }
    },
};
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
