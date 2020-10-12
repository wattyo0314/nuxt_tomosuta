<template>
  <div class="container">
    <input placeholder="タスクを追加" @keyup.enter="addTodo" />
    <ul>
      <li v-for="todo in todos" :key="todo.id">
        {{ todo.text }}
        <span><input type="checkbox" /></span>
      </li>
    </ul>
  </div>
</template>

<style lang="css"></style>

<script>
import { mapMutations } from "vuex";
export default {
  methods: {
    addTodo(e) {
      this.$store.commit("todos / add", e.target.value);
    },
  },
  computed: {
    todos() {
      return this.$store.state.todos.list;
    },
  },
};
</script>
