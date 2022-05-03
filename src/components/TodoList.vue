<template>
  <q-list class="q-py-md q-px-xl">
    <TodoItem v-for="todo in todos" :key="todo" :todo="todo" />
  </q-list>
</template>

<script>
import { defineComponent } from "vue";
import TodoItem from "./TodoItem";

export default defineComponent({
  props: ["todos"],
  components: {
    TodoItem,
  },
  setup() {
    return {};
  },
});
</script>
