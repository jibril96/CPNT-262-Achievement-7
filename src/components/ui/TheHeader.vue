<template>
  <h1>{{props.theHeader}}</h1>
</template>

<script setup>
   import {defineProps} from 'vue';
   const props = defineProps({
     theHeader:{
       type: String,
       default:'Welcome!'
     },
     
   });
   </script>

   <style>
   h1 {
       width: 100%;
    color: rgb(116, 16, 16);
    text-align: center;
   }
   </style>