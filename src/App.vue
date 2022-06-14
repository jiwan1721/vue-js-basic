<template>
<div id="app">
  <!-- <Todos id="1" title="basic" completed="true"/> -->
  <h1>To-do-list</h1>
  <ul>
    <li>
      <Done-First label="are you ready" :done="true"></Done-First>
    </li>
  </ul>
  <ul>
  <li v-for="item in ToDoItems" :key="item.id">
    <Done-First label="My ToDo Item" :done="true"></Done-First>
  </li>
</ul>

</div>

</template>

<script>
import DoneFirst from './components/DoneFirst.vue'

  export default {
    name: 'app',
    components: {
      DoneFirst
    },
    data(){
      return {
        DoneFirsts: [
          { id: uniqueId('todo-'), label: 'Learn Vue', done: false },
          { id: uniqueId('todo-'), label: 'Create a Vue project with the CLI', done: true },
          { id: uniqueId('todo-'), label: 'Have fun', done: true },
          { id: uniqueId('todo-'), label: 'Create a to-do list', done: false }
        ]
      }
    }
  
  };
</script>

<style scoped>
  /* *{
    box-sizing: border-box;
    margin:0;
    padding:0;
  }
  body {
    font-family: Arial,Helvetica,sans-serif;
    line-height:1.4;
  } */
</style>
