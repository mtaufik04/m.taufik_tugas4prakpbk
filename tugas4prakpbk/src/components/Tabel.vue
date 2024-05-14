<template>
  <div>
    <table>
      <thead>
        <tr>
          <th>No.</th>
          <th>Nama</th>
          <th>NIM</th>
          <th>Jurusan</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(student, index) in students" :key="student.id" class="table-row">
          <td>{{ index + 1 }}</td>
          <td>{{ student.nama }}</td>
          <td>{{ student.npm }}</td>
          <td>{{ student.jurusan }}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script setup>
import { ref, defineProps, defineEmits } from 'vue';

const props = defineProps({
  students: Array
});

const emit = defineEmits(['show-students']);
</script>
