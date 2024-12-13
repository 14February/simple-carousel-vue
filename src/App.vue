<script setup>
import { computed, reactive, ref } from 'vue';



const value1 = ref(0)

function jump(value) {
  value1.value = value
  console.log(value1.value)
}

</script>

<template>
  <img :src="`/${value1}.webp`" alt="图片">

  <ul>
    <li v-for="value in 4">
      <a href="#" @click.prevent="jump(value)">{{ value }}</a>
    </li>
  </ul>

</template>

<style scoped>

</style>
