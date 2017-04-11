<template>
  <div class="navigator-container">
    <ul>
      <li v-for="tab in tabs" v-on:click="tabSelected(tab)">{{tab.title}}</li>
    </ul>
  </div>
</template>

<script>
  export default {
    name: 'navigator',
    data: function(){
      return {
        tabs: [
          {'title': 'Tab 1', 'content':'Tab1 content'},
          {'title': 'Tab 2', 'content':'Some random text'},
          {'title': 'Tab 3', 'content':'slkdfjlskdjflsakdfj'}
        ]
      }
    },
    methods: {
        tabSelected: function(tab){
          this.$emit('tabchange', tab.content)
        }
    }
  }
</script>

<style scoped>
  .navigator-container {
  }
  ul {
    list-style-type: none;
    display: block;
  }
  li {
    display: inline;
    padding: 5px;
    border: 1px solid beige;
    cursor: pointer;
  }
  li:hover {
    background-color: beige;
  }
</style>
