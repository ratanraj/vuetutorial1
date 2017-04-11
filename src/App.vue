<template>
  <div id="app">
    <navigator v-on:tabchange="changeTheTab"></navigator>
    <nav-tab v-bind:content='currentTabContent'></nav-tab>
  </div>
</template>

<script>
import Hello from './components/Hello'
import TodoList from './components/TodoList'
import navigator from './components/navigator'
import tab from './components/tab'

export default {
  name: 'app',
  components: {
    'a-hello': Hello,
    'todo-list': TodoList,
    'navigator': navigator,
    'nav-tab': tab
  },
  data: function () {
      return {
          currentTabContent:''
      }
  },
  methods: {
      changeTheTab: function(content) {
        this.currentTabContent = content
      }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
}
</style>
