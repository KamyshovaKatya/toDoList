<template>
  <div id="app">
    <TodoList v-bind:todos="todos" v-on:delete-todo="deleteTodo"/>
  </div>
</template>

<script>
import TodoList from './components/TodoList.vue'

export default {
  name: 'app',
  data(){
    return {
      todos: ['Встать с кровати', 'Завтрак', 'Школа', 'Обед', 'Уборка', 'Домашняя работа', 'ШП', 'Ужин', 'Фильм', 'Сон']
    }
  },
  components: {
    TodoList
  },
  methods: {
    deleteTodo(index){
      this.todos.splice(index, 1);
    }
  }
}
</script>

<style>
#app {
        width: 700px;
        margin: auto;
        font-family: 'Arial', sans-serif;
        font-size: 18px;
        color: #35495e;
    }
</style>