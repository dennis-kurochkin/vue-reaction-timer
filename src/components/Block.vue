<template>
  <div class="block">
    Click me!
  </div>
</template>

<script>
export default  {
  props: [
      'delay',
  ],
}
</script>

<style>
  .block {
    width: 400px;
    -webkit-border-radius: 20px;
    -moz-border-radius: 20px;
    border-radius: 20px;
    color: #ffffff;
    background: #0faf87;
    text-align: center;
    padding: 100px 0;
    margin: 40px auto;
  }
</style>
