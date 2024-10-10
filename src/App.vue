<!-- vbase-3-ts-se -->\

<script setup lang="ts">
import { reactive, ref } from 'vue';


//สร้าง ref สำหรับเก็บข้อมูล count
const count = ref(0)
const myuser = ref({
  name: 'Natthpat Phummek',
  age: 22
})

// เก็บ array
const items = ref([1, 2, 3, 4, 5])

// สร้าง reactive สำหรับเก็บข้อมูล user
const user = reactive({
  name: 'Fes F1',
  age: 21
})


</script>

<template>
  
  <button @click="count++">+ Increment</button>
  <h1>Counter: {{ count }}</h1>
  <button @click="count--">- Decrement</button>

  <h1>{{ user.name }} {{ user.age }}</h1>
  <h1>{{ myuser.name }} {{ myuser.age }}</h1>

  <ul>
    <li v-for="items in items" :key="items">{{ items }}</li>
  </ul>

</template>

<style scoped>

</style>