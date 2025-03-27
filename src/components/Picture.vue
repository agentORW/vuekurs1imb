<script setup>
import { defineProps } from 'vue'

const props = defineProps({
  imageSrc: {
    type: String,
    required: true
  },
  imageTitle: {
    type: String,
    default: 'Image title'
  },
  imageDescription: {
    type: String,
    default: 'Image description'
  }
})
</script>

<template>
    <div class="picture-box">
        <img :src="props.imageSrc" 
        :alt="props.imageDescription" 
        class="picture-box__image" />
        <h2 class="picture-box__title">{{ props.imageTitle }}</h2>
        <p class="picture-box__description">{{ props.imageDescription }}</p>
    </div>
</template>

<style scoped>
.picture-box {
    border: 1px solid #ccc;
    padding: 16px;
    text-align: center;
}

.picture-box__image {
    max-width: 100%;
    height: 15rem;
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