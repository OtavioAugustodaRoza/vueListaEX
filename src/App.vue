<script setup>
import hello from './components/hello.vue';
import contador from './components/contador.vue';
import contadorInput from './components/contadorInput.vue';

</script>

<template>
  <div class="cont">
   <contadorInput/>
  </div>


 
  



</template>

<style scoped>
.cont{
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  height: 100dvh;
  background: linear-gradient(90dg, blue, purple,pink);
  gap: 30px;
}
</style>