<script setup>
import {ref} from 'vue';

const contador = ref(0);

const ac = (() => {
    contador.value++
})
const dc = (() => {
    if (contador.value > 0) {
        contador.value--
    }
})
</script>

<template>
      <div class="Dc">
        <h1>{{ contador }}</h1>
      </div>
  
      <div class="Db">
        <button @click="ac" class="btn">acrescentar</button>
        <button @click="dc" class="btn">decrementar</button>
      </div>
  </template>
  

  <style scoped>
 
.Dc{
    text-align: center;
}
.Db{
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 30px;
}
  
  h1 {
    font-size: 60px;
    font-weight: bold;
    color: #42b883;
  }
  
 
  
  .btn {
    background-color: #42b883;
    color: white;
    border: none;
    padding: 15px 30px;
    border-radius: 12px;
    cursor: pointer;
    font-size: 16px;
    transition: all 0.3s ease;
  }
  
  .btn:hover {
    background-color: #369870;
    transform: scale(1.05);
  }

  </style>
  