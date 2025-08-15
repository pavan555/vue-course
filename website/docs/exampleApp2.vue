<script setup>
import { ref, reactive } from 'vue'

// component logic
// declare some reactive state here.
  const message = ref("Hey Make me dynamic")
  
  const onMessageClick = () =>{
    console.log("clicked")
    message.value="Dynamically Changed"
  }
  const count = reactive({
    counter: 0
  })
  const increment = () => {
    count.counter++;
  }
  const decrement = () => {
    count.counter--;
  }
  
  const reset = () => {
    count.counter=0;
  }
  
</script>

<template>
  <h1 v-on:click="onMessageClick">{{message.split("").reverse().join("")}}</h1>
  <p>
    Counter is : {{count.counter}}
  </p>
  <button v-on:click="increment">
    Increment
  </button>
  <button v-on:click="reset">
    Reset
  </button>
  <button v-on:click="decrement">
    Decrement
  </button>
</template>
