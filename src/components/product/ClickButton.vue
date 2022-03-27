<template>
  <div class="click">
    <a href="#">
     <button>
      <slot></slot>
     </button>
    </a>
  </div>
</template>

<script setup></script>

<style>
.click {

  padding: 0.75rem;
  background: yellow;
  color: white;
  border-radius: 1rem;
  font-weight: 600;

}

.click:hover {
  background: red;
}
</style>

<script setup></script>