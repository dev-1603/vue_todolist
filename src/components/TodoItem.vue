<template>
  <div class="todo-item" :class="{'is-complete':todo.completed}">
    <p>
      <input type="checkbox" @change="markComplete" @click="$emit('del-todo', todo.id)" :checked="todo.completed">
      <label >{{todo.title}}</label>
     
      </p>
  </div>
</template>

<script>
export default {
  name: "TodoItem",
  props: ["todo"],
  methods: {
    markComplete() {
      this.todo.completed = !this.todo.completed;
      
    }
  }
}
</script>

<style scoped>
  .todo-item {
    background: #f4f4f4;
    padding: 10px;
    border-bottom: 1px #ccc dotted;
  }

  .is-complete {
    text-decoration: line-through;
  }

  
</style>

