<template>
<div class="img">
  <img
    :src="props.url"
    :alt="props.alt"
  />
</div>
</template>

<script setup>
import {defineProps} from 'vue';
  const props = defineProps({
    url: {
      type: String,
      required: true,
    },
    alt: {
      type: String,
    },
  });
</script>

<style>
.img {
    position: relative;
    width: 100%;
    max-width: 320px;
    background: #fff;
    border: 1px solid #ddd;
    transition: border-color 0.25s, box-shadow 0.25s;
    display: flex;
    flex-direction: column;
}
</style>
