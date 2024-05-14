<script setup>
import Emits from './components/Emits.vue'
import SlotComponent from './components/Slot.vue';
</script>

<template>
  <div>
    <SlotComponent title="Contoh Slot Component">
      <p class="data-mahasiswa">DATA MAHASISWA</p>
      <p class="author">TUGAS<span class="highlight"></span><span class="highlight-first">4. PRAKTIKUM</span> <span class="highlight-last">PBK</span></p>
    </SlotComponent>
  </div>
  <Datatabel />
  <Buttom />
  <Emits />
</template>

<style scoped>
  .data-mahasiswa {
    font-size: 24px;
    font-weight: bold;
    color: #333;
    background-color: transparent;
    padding: 10px 20px;
    border-radius: 5px;
    text-align: center;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    backdrop-filter: blur(5px);
    transition: transform 0.3s ease;
    margin-bottom: 20px;
  }
  .data-mahasiswa:hover {
    transform: scale(1.1);
  }
  .author {
    font-family: 'Montserrat', sans-serif;
    position: absolute; /* Mengatur posisi absolut */
    top: 0; /* Di pojok atas */
    left: 0; /* Di pojok kiri */
    margin: 10px;
    color: #603c04;
    font-size: 22px; /* Ubah ukuran font */
  }
  .highlight {
    color: #ff6347;
    font-size: 32px;
    font-weight: bold;
  }
  .highlight-first, .highlight-last {
    font-family: 'Pacifico', cursive;
    font-style: italic;
    text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.3);
  }
</style>
