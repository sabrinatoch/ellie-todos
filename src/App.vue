<script setup lang="ts">
import { RouterView } from 'vue-router';
import  TodoHeader  from './components/TodoHeader.vue';
</script>

<template>
  <TodoHeader/>
  <RouterView />
</template>

<style lang="scss">
@import './assets/styles.scss';
</style>