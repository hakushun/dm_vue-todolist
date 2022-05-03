<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated class="glossy">
      <q-toolbar>
        <q-toolbar-title> Todo App</q-toolbar-title>
      </q-toolbar>
    </q-header>

    <q-page-container>
      <TodoForm :todos="todos" />
      <TodoList :todos="todos" />
    </q-page-container>
  </q-layout>
</template>

<script>
import { ref } from "vue";
import TodoForm from "./components/TodoForm.vue";
import TodoList from "./components/TodoList.vue";

export default {
  name: "LayoutDefault",
  components: {
    TodoForm,
    TodoList,
  },
  setup() {
    const todos = ref([]);

    return { todos };
  },
};
</script>
