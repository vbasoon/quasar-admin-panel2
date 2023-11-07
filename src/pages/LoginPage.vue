<template>
  <q-page class="flex flex-center" padding>
    <q-card class="full-width" style="max-width: 400px">
      <q-card-section style="font-size: 1.3em" class="text-center">
        Login
      </q-card-section>
      <q-card-section>
        <q-input filled label="Name" class="q-mb-md" v-model="form.email" />
        <q-input
          filled
          label="Password"
          type="password"
          v-model="form.password"
        />
      </q-card-section>
      <q-btn
        class="full-width"
        label="Login"
        color="primary"
        @click="login"
      ></q-btn>
    </q-card>
  </q-page>
</template>

<script setup>
import { ref } from "vue";
const form = ref({
  email: "",
  password: "",
});

function login() {
  console.log(form.value);
  // axios.post("/login");
  // form.value;
}
</script>
