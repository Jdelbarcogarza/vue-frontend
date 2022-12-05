<template>
  <div class="home center">
    <form class="container">
      <label for="name">Escribe tu nombre</label>
      <input id="name" type="text" placeholder="nombre" v-model="name" />
      <button type="submit" @click="handleSubmit">Submit</button>
    </form>
  </div>
</template>

<script setup>
import { ref } from "vue";

const name = ref("");

// eslint-disable-next-line no-unused-vars
const handleSubmit = (event) => {
  event.preventDefault();
  console.log("enviado", name.value);
};
</script>

<style scoped>
.center {
  display: flex;
  justify-content: center;
}
.container {
  display: flex;
  flex-direction: column;
  width: fit-content;
}
</style>
