<script setup>
import PictureBox from './components/Picture.vue'

function getImageUrl(name) {
  return new URL(`./assets/${name}`, import.meta.url).href
}
</script>

<template>
  <h1>Fotogalleri</h1>

  <PictureBox 
  :imageSrc="getImageUrl('flower.png')"
  imageTitle="Blomst"
  imageDescription="En fantastisk blomst som jeg lagde i teknologiforståelse i fjor"/>

  <PictureBox 
  :imageSrc="getImageUrl('flower.png')"/>

</template>

<style>
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    background-color: #f4f4f4;
    color: #333;
}

h1 {
    font-size: 2.5em;
    color: #333;
    text-align: center;
    margin-top: 20px;
    margin-bottom: 20px;
    text-transform: uppercase;
    letter-spacing: 2px;
}
</style>
