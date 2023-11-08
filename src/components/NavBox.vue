<template>
    <div class="nav-box">
      <h3>{{ caption }}</h3>
      <ul>
        <li v-for="(item, index) in items" :key="index">
          <a :href="item.link">{{ item.text }}</a>
        </li>
      </ul>
    </div>
  </template>
  
  <script lang="ts">
  export default {
    props: {
      caption: String, 
      items: Array, 
    },
  };
  </script>
  
  <style scoped>
  .nav-box {
    border: 1px solid #ccc;
    padding: 10px;
    margin: 5px 0;
  }
  </style>