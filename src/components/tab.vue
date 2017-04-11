<template>
  <div>
    <h2>Content:</h2>
    <p>
      {{content}}
    </p>
  </div>
</template>

<script>
export default {
  props: ['content']
}
</script>

<style scoped>
  div {
    float: none;
  }
</style>
