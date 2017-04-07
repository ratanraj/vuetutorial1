<template>
  <div>
    <h2>TO DO({{numberOfTasks}})</h2>
    <div>{{doneTasks}} tasks completed</div>
    <table border="1">
      <tr>
        <th>Title</th>
        <th>Description</th>
        <th>Done</th>
      </tr>
      <tr v-for="todoitem in todo" v-bind:class="{done: todoitem.done, reditem: !todoitem.done}">
        <td>{{todoitem.title}}</td>
        <td>{{todoitem.desc}}</td>
        <td><input type="checkbox" v-model="todoitem.done"></td>
        <td><button v-on:click="removeTodoItem($index)">remove</button></td>
      </tr>
      <tr>
        <td>
          <input v-model="title">
        </td>
        <td>
          <input v-model="desc">
        </td>
        <td>
          <button v-on:click="addTodoItem()">Add</button>
        </td>
      </tr>
    </table>
  </div>
</template>

<script>
  export default {
    name: 'todo',
    data: function(){
        return {
            title: '',
            desc: '',
            todo:[
              {'title': 'Teach Vue','desc':'Create a project and ....', 'done': true},
              {'title': 'SOC2 Screenshots','desc':'Take screenshots for soc2 audit', 'done': false}
            ]
        }
    },
    computed: {
        numberOfTasks: function(){
            return this.todo.length
        },
        doneTasks: function(){
            var count_of_completed_tasks = 0
            for(var i in this.todo) {
                if(this.todo[i].done) {
                    count_of_completed_tasks++
                }
            }
            return count_of_completed_tasks
        }
    },
    methods: {
        addTodoItem: function(){
            this.todo.push({'title':this.title, 'desc':this.desc, 'done': false})
            this.title = ''
            this.desc = ''
        },

        removeTodoItem: function(index) {
            this.todo.splice(index, 1)
        }
    }
  }
</script>

<style>
.done {
  text-decoration: line-through;
}
  .reditem {
    background-color: red;
  }
</style>
