<template>
  <q-item clickable v-ripple>
    <q-item-section>{{ todo }}</q-item-section>
  </q-item>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  props: ["todo"],
  setup() {
    return {};
  },
});
</script>
