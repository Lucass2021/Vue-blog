<template>
  <div>
    <HeaderComponent/>
    <PostsBodyComponent/>
    <!-- Information: -->
    <!-- <font-awesome-icon :icon="['fas', 'search']" />
    <font-awesome-icon :icon="['fas', 'heart']" />
    <font-awesome-icon :icon="['far', 'heart']" /> -->
    <!-- font-family: 'Inter', sans-serif; -->
  </div>
</template>

<script setup>
import HeaderComponent from './components/HeaderComponent.vue';
import PostsBodyComponent from './components/PostsBodyComponent.vue';


</script>

<style>
  * {
      margin:0;
      padding:0;
      box-sizing: border-box;
    }

</style>