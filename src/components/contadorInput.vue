<script setup> 
import { ref} from 'vue';



const texto = ref('')





const resetar = (() => {
    texto.value = '';
})




</script>
<template>
    <div>
        <h1>{{ texto.length }}</h1>
    </div>
    <div>
        <input v-model="texto" type="text" placeholder="digite algo">
    </div>
    <div>
        <button class="btn" @click="resetar" >reset</button>
    </div>
    <div>
        <h2 v-if="texto.length == 0">Digite algo</h2>
    </div>

</template>
 <style scoped>
 h1{
    font-weight: bold;
    color: #42b883;
    font-size: 60px;
 }
 input{
    padding: 10px;
    border: 2px solid #ccc;
    border-radius: 5px;
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