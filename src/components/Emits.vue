<template>
    <div>
      <Button @show-students="handleShowStudents" />
      <Tabel v-if="displayStudents" :students="students" />
      <Tabel v-if="displayStudents" :students="students" />
    </div>
  </template>
  
  <script setup>
  import Button from './Buttom.vue';
  import Tabel from './Tabel.vue';
  import { ref } from 'vue';
  
  const students = ref([]);
  
  const handleShowStudents = () => {
   
  };
  </script>
  