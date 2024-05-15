<template>
  <div class="slot-component">
    <h2>{{ title }}</h2>
    <slot></slot>
  </div>
</template>

<script setup>
const props = {
  title: String
};
</script>

<style scoped>
.slot-component {
  border: 1px solid #ccc;
  padding: 20px;
  margin-bottom: 20px;
}
</style>
