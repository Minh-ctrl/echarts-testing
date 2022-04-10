<script setup>
import pieChart from '../components/pieChart.vue';
import lineChart from '../components/lineChart.vue'
import Test from '../components/Test.vue'
</script>
<template>
  <div class="about">
    <h1>This is an about page</h1>
    <!-- <pieChart/> -->
    <Test/>
  </div>
</template>
<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}
</style>
