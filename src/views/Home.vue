<template>
  <div id="app">
    <AddTodo @add-todo="addTodo" />
    <Todos :todos="todos" @del-todo="deleteTodo" />
  </div>
</template>

<script>
import Todos from '../components/Todos';
import AddTodo from '../components/AddTodo';
import axios from 'axios';

export default {
  name: 'Home',
  components: {
    Todos,
    AddTodo
  },
  data() {
    return {
      todos: [
        {
          id: 1,
          title: "sample test",
          completed: false
        }
      ]
    }
  },
  methods: {
    deleteTodo(id) {
       this.todos = this.todos.filter(todo => todo.id !== id);
      
    },
    addTodo(newTodo) {
      this.todos = [...this.todos, newTodo];     }
  }
  
}
</script>

<style>
  * {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }

  body {
    font-family: Arial, Helvetica, sans-serif;
    line-height: 1.4;
  }

  .btn {
    display: inline-block;
    border: none;
     background: rgb(255, 0, 0);
    color: #fff;
    padding: 7px 20px;
    cursor: pointer;
  }

  .btn:hover {
   background: rgb(48, 155, 21);
  }
</style>
