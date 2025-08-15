<script setup>
import { ref } from 'vue'

const titleClass = ref('title')
</script>

<template>
  <h1 :class="titleClass">Make me red</h1> <!-- add dynamic class binding here -->
</template>

<style>
.title {
  color: red;
  background-color: aqua;
  box-shadow:2px 4px;
  padding: 20px;
  font-family: arial;
}
</style>
