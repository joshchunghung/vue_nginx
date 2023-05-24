<script setup>
// import calendar from '@/componen/ts/calendar.vue';
import { onBeforeMount, onBeforeUnmount, onUnmounted } from 'vue';
let i = 0;
let count = setInterval(function () {  // count = ID值
  console.log(i);
  i++
}, 1000);

onBeforeUnmount(() => {
  clearInterval(count);
})
</script>
<template>
  123
</template>


