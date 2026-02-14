<script setup>
import { ref } from 'vue'

const texto = ref('')
const tarefas = ref([])

const Adicionar = () => {
    if(texto.value !== ""){
  const tarefa = {
    ta: texto.value,
  }
  tarefas.value.push(tarefa)
  texto.value = ''
}else{
    alert("digite algo")
}}
const remover = ((i) => {
    tarefas.value.splice(i,1)
})
</script>
<template>
  <div class="main">
    <input v-model="texto" type="text" placeholder="digite sua tarefa" />
    <button @click="Adicionar" class="btn">Adicionar tarefa</button>
  </div>
  <div class="te"> 
    <ul>
    <li v-for="(tarefa, index) in tarefas" :key="index" class="lista">
      {{ tarefa.ta }} <button @click="remover(index)" class="btn">excluir</button>
    </li>
  </ul>
</div>
 
</template>
<style scoped>
.main {
  display: flex;
  gap: 15px;
  justify-content: center;
  margin-top: 40px;
}

.te {
  margin-top: 40px;
  display: flex;
  justify-content: center;
}

ul {
  list-style: none;
  padding: 0;
  width: 400px;
  display: flex;
  flex-direction: column;
  gap: 15px;
}

.lista {
  background: white;
  padding: 15px 20px;
  border-radius: 12px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.08);
  display: flex;
  justify-content: space-between;
  align-items: center;
  font-size: 18px;
  font-weight: 500;
  color: #2c3e50;
}

input {
  padding: 12px;
  width: 250px;
  border: 2px solid #ddd;
  border-radius: 8px;
  outline: none;
  transition: 0.3s;
}

input:focus {
  border-color: #42b883;
}

.btn {
  background-color: #42b883;
  color: white;
  border: none;
  padding: 10px 18px;
  border-radius: 8px;
  cursor: pointer;
  font-size: 14px;
  transition: all 0.3s ease;
}

.btn:hover {
  background-color: #369870;
  transform: scale(1.05);
}

</style>
