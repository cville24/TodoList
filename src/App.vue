<template>
  <div id="app-2">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld :msg="msg2"/>
    <AddTodo @addTodo="onAddTodo"/>
    <TableToDo :tasks="tasks"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import AddTodo from './components/AddTodo.vue'
import TableToDo from './components/TableToDo'

export default {
  name: 'App',
  components: {
    HelloWorld,
    AddTodo,
    TableToDo
  },
  data: ()=>({
    msg2: "Todo List",
    tasks: []
  }),
  methods: {
    onAddTodo: function(task){
      this.tasks = [...this.tasks, task];
      }
  }
}
</script>

<style>
#app-2 {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
