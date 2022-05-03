<template>
  <form @submit.prevent="onSubmit" class="q-py-md q-px-xl">
    <q-input filled v-model="input" />
    <q-btn color="primary" label="add" type="submit" />
  </form>
</template>

<script>
import { defineComponent, ref, toRefs } from "vue";

export default defineComponent({
  props: ["todos"],
  setup(props) {
    const { todos } = toRefs(props);
    const input = ref("");

    const onSubmit = () => {
      if (input.value.trim() === "") return;
      todos.value.push(input.value.trim());
      input.value = "";
    };

    return { input, onSubmit };
  },
});
</script>
