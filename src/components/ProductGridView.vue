<script lang="ts">
import tovar from '../tovar.json'
export default {
  data() {
    return {
    tovars:tovar,
    };
  },
};
console.log(tovar)
console.log("Vue is my crash")
</script>
<template>

<div class="product-main" >

<h2 class="title">Товар со скидкой</h2>

<div class="product-grid">

  <div class="showcase"  v-for="tovar in tovars" :key="tovar.id">

    <div class="showcase-banner">

      <img :src="tovar.img" alt="PC" width="300" class="product-img default">
      <img :src="tovar.img_hover" alt="PC" width="300" class="product-img hover">

      <p class="showcase-badge">15%</p>

      <div class="showcase-actions">

        <button class="btn-action">
          <ion-icon name="heart-outline"></ion-icon>
        </button>

        <button class="btn-action">
          <ion-icon name="eye-outline"></ion-icon>
        </button>

        <button class="btn-action">
          <ion-icon name="repeat-outline"></ion-icon>
        </button>

        <button class="btn-action">
          <ion-icon name="bag-add-outline"></ion-icon>
        </button>

      </div>

    </div>

    <div class="showcase-content">

      <a href="#" class="showcase-category">{{tovar.name}}</a>

      <a href="#">
        <h3 class="showcase-title">{{ tovar.opisanie }}</h3>
      </a>

      <div class="showcase-rating">
        <ion-icon name="star"></ion-icon>
        <ion-icon name="star"></ion-icon>
        <ion-icon name="star"></ion-icon>
        <ion-icon name="star-outline"></ion-icon>
        <ion-icon name="star-outline"></ion-icon>
      </div>

      <div class="price-box">
        <p class="price" >{{ tovar.price }}</p>
        <del>{{ tovar.proshlaya_cena }}</del>
      </div>

    </div>

  </div>

  
</div>

</div>





</template>
<style>
@import '../assets/main.css';
</style>