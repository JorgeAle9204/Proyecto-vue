<template>
  <div>
 <h1>Contador</h1> 
<p>{{ contador }}</p>
<button @click="incrementar()"> Incrementar</button>
<button @click="decrementar()"> Decrementar</button>
</div>
</template>

<script setup>

import {ref} from 'vue'
const contador = ref (0)
const incrementar = () => {
      contador.value++
}
const decrementar = () => {
  contador.value--
}

</script>

<style scoped>
p {
  color: red
}
</style>
