<template>
    <div>
      <button @click="handleClick" class="button">{{ buttonText }}</button>
      <Tabel v-if="displayStudents" :students="students" @show-students="$emit('show-students')" />
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  import Tabel from './Tabel.vue';
  
  const students = ref([
    { id: 1, nama: 'M.TAUFIK KURRAHMAN', npm: '223510370', jurusan: 'TEKNIK INFORMATIKA' },
    { id: 2, nama: 'Jane Smith', npm: '223510321', jurusan: 'TEKNIK SIPIL' },
    { id: 3, nama: 'Alice Johnson', npm: '223510765', jurusan: 'TEKNIK ELEKTRO' }
  ]);
  const buttonText = 'Lihat Data Mahasiswa';
  const displayStudents = ref(false);
  
  const handleClick = () => {
    displayStudents.value = true;
    alert('Data mahasiswa berhasil dipanggil!');
  };
  </script>
  
  <style scoped>
  .button {
    background-color: #4CAF50;
    border: none;
    color: white;
    padding: 15px 32px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
    margin: 4px 2px;
    cursor: pointer;
    border-radius: 8px;
  }
  
  .button:hover {
    background-color: #45a049;
  }
  </style>
  