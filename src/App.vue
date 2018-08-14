<template>
  <div id="app">
    <img width="25%" src="./assets/logo.png">
    <h1>Vue Todo list</h1>
    <TodoList/>
  </div>
</template>

<script>
import TodoList from "./components/TodoList";

export default {
  name: "App",
  components: {
    TodoList
  }
};
</script>

<style>
  #app{
    margin: 0 auto; 
    display: block;
  }

h1{
  text-align: center;
}
  img{
    display: block;
    margin: 0 auto;
  }
</style>
