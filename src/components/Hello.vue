<template>
  <div>
    <input v-model="classname">
    <h2 v-bind:class="classname">{{message}}</h2>
    <h2 class="redelement"></h2>
  </div>
</template>

<script>
export default {
  name: 'hello',
  data: function(){
      return {
          message: 'Hello! This is a component!',
          classname: 'redelement'
      }
  }
}
</script>

<style scoped>
  .redelement {
    color: red;
  }
  .blueelement {
    color: blue;
    border: 1px solid blue;
  }
</style>
