<template>
<div class="design">
  <article>
    <slot></slot>
  </article>

</div>
</template>

<script setup>
</script>

<style>
.design  {

    display: flex;
    place-items: center;
    gap: 1rem;
    width: 50rem;
  min-width: 768px;
  background-color: white;
    margin: 24px 24px;
    padding: 24px 24px;
    border-radius: 24px;
border-radius: 24px;
}
</style>