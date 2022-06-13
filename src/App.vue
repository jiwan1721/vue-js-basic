<template>
<div id="app">
  <!-- <Todos id="1" title="basic" completed="true"/> -->
  <h1>To-do-list</h1>
  <ul>
    <li>
      <Done-First label="are you ready"></Done-First>
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
