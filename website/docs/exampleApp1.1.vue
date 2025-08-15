<script>
import {ref} from 'vue'
export default {
  setup() {

    const count = ref(0);
    const increment = () => {
      count.value++;
    }
    return {
      count,
      increment
    }
  }
  
}
</script>

<template>
  <button @click="increment">Count is: {{ count }}</button>
</template>
