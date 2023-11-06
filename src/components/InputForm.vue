<template>
    <div class="mb-3">
      <label :for="inputId" class="form-label">{{ label }}</label>
      <input type="text" class="form-control" :id="inputId" :placeholder="inputPlaceholder">
    </div>
  </template>
  
  <script lang="ts">
  export default {
    name: 'InputForm',
    props: {
      label: String,             
      inputId: String,           
      inputPlaceholder: String,  
    },
  };
  </script>
  
  <style scoped>

  </style>