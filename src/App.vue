<script setup>

import { onMounted, ref } from 'vue';
import CityList from './components/CityList.vue';
import Navbar from './components/Navbar.vue';


let cityListData = ref([]);

onMounted(() => {
  fetch('https://cityinfoappnodejs.onrender.com/api')
    .then(response => response.json())
    .then(res => cityListData.value = res)
});

</script>

<template>
<div>
 <header>
   <Navbar />
  </header>

  <main>
    <div class="container">
      <CityList :citiesData="cityListData" />
    </div>
  </main>
</div>
  
</template>

<style scoped>
.container {
  padding: 15px;
}
</style>
