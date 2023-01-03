<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import Header from './components/Header.vue'
import ContentTwoVue from './components/ContentTwo.vue';
//import CategoriesViewVue from './components/CategoriesView.vue';
import BlogViewVue from './components/BlogView.vue';
import ProductGridViewVue from './components/ProductGridView.vue';
import ProductFeatureVue from './components/ProductFeature.vue';
import ServiceViewVue from './components/ServiceView.vue';
import FooterVue from './components/Footer.vue';
</script>

<template>
  <header>
  
<Header/>
<ContentTwoVue/>
<div class="wrapper">
     <nav>
       <RouterLink to="/">Категории</RouterLink>
       <RouterLink to="/about">Новые товары</RouterLink>
     </nav>
     <RouterView />
   </div>
<ProductGridViewVue/>
<BlogViewVue/>
<ProductFeatureVue/>
<ServiceViewVue/>
<FooterVue/>
</header>

  
</template>



