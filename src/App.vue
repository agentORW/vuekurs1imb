<script setup>
import { ref } from 'vue'
import PictureBox from './components/Picture.vue'
import reactImagePath from './assets/arireact.png'

const reactImage = ref(reactImagePath)
</script>

<template>
  <PictureBox 
  :imageSrc="reactImage" 
  imageAlt="React Logo"/>
  <h1>Yeah</h1>
</template>

<style>
</style>
