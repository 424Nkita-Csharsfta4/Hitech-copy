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

<div>

<div class="container">

  <div class="testimonials-box">
    <div class="service">

      <h2 class="title">Наши Сервисы</h2>

      <div class="service-container">

        <a href="#" class="service-item">

          <div class="service-icon">
            <ion-icon name="boat-outline"></ion-icon>
          </div>

          <div class="service-content">

            <h3 class="service-title">Доставка по всему ПМР</h3>
            <p class="service-desc">Для заказа свыше 100Р</p>

          </div>

        </a>

        <a href="#" class="service-item">
        
          <div class="service-icon">
            <ion-icon name="rocket-outline"></ion-icon>
          </div>
        
          <div class="service-content">
        
            <h3 class="service-title">Наследуйщий день доставка</h3>
           
        
          </div>
        
        </a>

        <a href="#" class="service-item">
        
          <div class="service-icon">
            <ion-icon name="call-outline"></ion-icon>
          </div>
        
          <div class="service-content">
        
            <h3 class="service-title">Лучшая онлайн-поддержка</h3>
            <p class="service-desc">Часы работы: с 8:00 до 19:00.</p>
        
          </div>
        
        </a>

        <a href="#" class="service-item">
        
          <div class="service-icon">
            <ion-icon name="arrow-undo-outline"></ion-icon>
          </div>
        
          <div class="service-content">
        
            <h3 class="service-title">Политика возврата</h3>
            <p class="service-desc">Простой и бесплатный возврат</p>
        
          </div>
        
        </a>

        <a href="#" class="service-item">
        
          <div class="service-icon">
            <ion-icon name="ticket-outline"></ion-icon>
          </div>
        
          <div class="service-content">
        
            <h3 class="service-title">30% Кэш бэк при регистрации</h3>
           
          </div>
        
        </a>

      </div>

    </div>

  </div>

</div>

</div>

</template>
<style>
@import '../assets/main.css';
</style>