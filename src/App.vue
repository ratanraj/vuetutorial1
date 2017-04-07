<template>
  <div id="app">
    <todo-list></todo-list>
  </div>
</template>

<script>
import Hello from './components/Hello'
import TodoList from './components/TodoList'

export default {
  name: 'app',
  components: {
    'a-hello': Hello,
    'todo-list': TodoList
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
}
</style>
