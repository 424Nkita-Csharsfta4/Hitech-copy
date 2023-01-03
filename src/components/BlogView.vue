<script lang="ts">
import tovar from '../tovar.json'
export default {
  data() {
    return {
    tovars:tovar,
    };
  },
};
</script>
<template>
  <div class="blog">

<div class="container">

  <div class="blog-container has-scrollbar">

    <div class="blog-card" v-for="tovar in tovars" :key="tovar.id">

      <a href="#">
        <img :src="tovar.img" alt="tovar" width="300" class="blog-banner">
      </a>

      <div class="blog-content">

        <a href="#" class="blog-category">{{ tovar.name }}</a>

        <a href="#">
          <h3 class="blog-title">{{ tovar.opisanie }}</h3>
        </a>

        <p class="blog-meta">
          <cite>HiTech</cite> / <time datetime="2023-01-02">Январь 02, 2023</time>
        </p>

      </div>

    </div>

 

  </div>

</div>

</div>

</template>
<style>
@import '../assets/main.css';
</style>