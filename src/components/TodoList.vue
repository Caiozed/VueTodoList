<template>
  <div class="todo-list" >
    <TodoForm @onsubmit="addItem"/>
    <ul>
      <li v-for="todo in todos">
        <Todo @delete="removeItem" :name="todo"/>
      </li>
    </ul>
  </div>
</template>

<script>
import Todo from "./Todo";
import TodoForm from "./TodoForm";

export default {
  data() {
    return {
      todos: ["This ia a list item"]
    };
  },

   components: {
    Todo,
    TodoForm
  },

  methods: {
    addItem(todo){
      this.todos.push(todo);
    },

    removeItem(todo){
      this.todos = this.todos.filter(name => {
        return name !== todo;
      });
    }
  }
};
</script>

<style scoped>
  .todo-list{
    text-align: center;
  }

  ul{
    list-style: none;
  }
</style>
