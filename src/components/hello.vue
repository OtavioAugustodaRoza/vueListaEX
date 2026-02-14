<script setup>
import { ref } from 'vue'

const estado = ref(false)

const trocarCor = () => {
  estado.value = !estado.value
}
</script>

<template>
  <div class="center">
    <button @click="trocarCor()" :class="{ padrao: !estado, alterada: estado }">HELLO WORLD</button>
  </div>
</template>

<style scoped>
.center {
  align-items: center;
  justify-content: center;
}
.padrao {
  background-color: #42b883;
  color: white;
  border: none;
  padding: 20px 20px;
  border-radius: 10px;
  cursor: pointer;
}
.alterada {
  background-color: blueviolet;
  color: white;
  border: none;
  padding: 20px 20px;
  border-radius: 10px;
  cursor: pointer;
}
</style>
