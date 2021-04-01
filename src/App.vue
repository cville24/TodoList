<template>
  <div id="app-2">
    <img alt="Vue logo" src="./assets/logo.png">
    <HelloWorld :msg="msg2"/>
    <InputList @event="getTask"/>
    {{ task }}
    <TableToDo />
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import InputList from './components/InputList.vue'
import TableToDo from './components/TableToDo'

export default {
  name: 'App',
  components: {
    HelloWorld,
    InputList,
    TableToDo
  },
  data: ()=>({
    msg2: "Todo List",
    task: null
  }),
  methods: {
    getTask: function(value){
      this.task = value;
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
