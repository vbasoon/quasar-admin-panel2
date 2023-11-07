<template>
  <q-page class="flex flex-center column">
    <h1>One Page</h1>
    <input type="text" v-model="myVar" />
    <pre>Output: {{ myVar }}</pre>
    <pre>{{ computedName }}</pre>

    <q-btn @click="changeMyOption"> Change! </q-btn>
  </q-page>
</template>

<script setup>
import { ref, computed } from "vue";

const myVar = ref("");

const computedName = computed(() => {
  return myVar.value + " more more more...!";
});

function changeMyOption() {
  myVar.value = "Dark" + myVar.value;
}
</script>
