<template>
  <p class="result">
    Your result: {{ result }} ms
  </p>
</template>

<script>
export default  {
  props: {
    result: Number,
  }
}
</script>
