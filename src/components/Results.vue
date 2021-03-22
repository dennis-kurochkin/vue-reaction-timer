<template>
  <p class="result">
    Your result: {{ score }} ms
  </p>
  <h2>Your rank: {{ rank }}</h2>
</template>

<script>
export default {
  props: {
    score: Number,
  },
  data() {
    return {
      rank: null,
    }
  },
  mounted() {
    if (this.score < 250) {
      this.rank = 'Ninja Fingers!';
    } else if (this.score < 400) {
      this.rank = 'Rapid Reflexes';
    } else {
      this.rank = 'Snail pace...';
    }
  }
}
</script>
