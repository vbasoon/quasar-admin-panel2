<template>
  <q-page class="flex flex-center">
    <h1>{{ myMessage }}</h1>
  </q-page>
</template>

<script>
import { defineComponent, ref } from "vue";

export default {
  name: "ThreePage",
  setup() {
    const myMessage = ref("My reactive message");
    return {
      myMessage,
    };
  },
};
</script>
