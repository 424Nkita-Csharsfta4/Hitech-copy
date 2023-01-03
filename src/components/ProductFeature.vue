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
<div class="product-featured">

<h2 class="title">Распродажа</h2>

<div class="showcase-wrapper has-scrollbar">

  <div class="showcase-container" v-for="tovar in tovars" :key="tovar.id">

    <div class="showcase">
      
      <div class="showcase-banner">
        <img :src="tovar.img" alt="tovar" class="showcase-img">
      </div>

      <div class="showcase-content">
        
        <div class="showcase-rating">
          <ion-icon name="star"></ion-icon>
          <ion-icon name="star"></ion-icon>
          <ion-icon name="star"></ion-icon>
          <ion-icon name="star-outline"></ion-icon>
          <ion-icon name="star-outline"></ion-icon>
        </div>

        <a href="#">
          <h3 class="showcase-title">{{ tovar.name }}</h3>
        </a>

        <p class="showcase-desc">
        {{ tovar.opisanie }}
        </p>

        <div class="price-box">
          <p class="price">{{ tovar.price }}</p>

          <del>{{ tovar.proshlaya_cena }}</del>
        </div>

        <button class="add-cart-btn">Добавить карту</button>

        <div class="showcase-status">
          <div class="wrapper">
            <p>
             Купили: <b>20</b>
            </p>

            <p>
              Осталось: <b>40</b>
            </p>
          </div>

          <div class="showcase-status-bar"></div>
        </div>

        <div class="countdown-box">

          <p class="countdown-desc">
            ТОРОПИТЬСЯ! ПРЕДЛОЖЕНИЕ ЗАКАНЧИВАЕТСЯ ЧЕРЕЗ:
          </p>

          <div class="countdown">

            <div class="countdown-content">

              <p class="display-number">60</p>

              <p class="display-text">Дней</p>

            </div>

            <div class="countdown-content">
              <p class="display-number">24</p>
              <p class="display-text">Часа</p>
            </div>

            <div class="countdown-content">
              <p class="display-number">59</p>
              <p class="display-text">Минут</p>
            </div>

            <div class="countdown-content">
              <p class="display-number">00</p>
              <p class="display-text">Секунд</p>
            </div>

          </div>

        </div>

      </div>

    </div>

  </div>


</div>

</div>

</template>
<style>
@import '../assets/main.css';
</style>