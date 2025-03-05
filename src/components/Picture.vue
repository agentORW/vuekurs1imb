<template>
    <!-- <div class="picture-box">
        <img :src="`./assets/${image}`" alt="Picture" class="picture-box__image" />
        <h2 class="picture-box__title">{{ title }}</h2>
        <p class="picture-box__description">{{ description }}</p>
    </div> -->
    <h1>{{ title }}</h1>
    <img 
      :src="props.imageSrc" 
      :alt="props.imageAlt" 
      class="picture"
    />
</template>

<script setup>
import { defineProps } from 'vue'

const props = defineProps({
  imageSrc: {
    type: String,
    required: true
  },
  imageAlt: {
    type: String,
    default: 'Image description'
  }
})
</script>

<style scoped>
.picture-box {
    border: 1px solid #ccc;
    padding: 16px;
    text-align: center;
}

.picture-box__image {
    max-width: 100%;
    height: auto;
}

.picture-box__title {
    font-size: 1.5em;
    margin: 16px 0 8px;
}

.picture-box__description {
    font-size: 1em;
    color: #666;
}
</style>