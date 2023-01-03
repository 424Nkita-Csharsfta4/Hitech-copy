<script setup lang="ts">
import { ref } from "vue";
let input = ref("");
const fruits = ["Клавиатура", "Мышка", "Телефон"];
function filteredList() {
  return fruits.filter((fruit) =>
    fruit.toLowerCase().includes(input.value.toLowerCase())
  );
}
const tovar_bitovaya_tehnika ={
  name_1:"Бытовая техника",
  name_2:"Холодильники",
  name_3:"Морозильники и лари",
  name_4:"Духовые шкафы",
  name_5:"Посудомоечные машины",
  name_6:"Микроволновые печи"
}
const tovar_PC={

  name_1:"Девайсы",
  name_2:"Планшеты",
  name_3:"Электронные книги",
  name_4:"Системные блоки",
  name_5:"Моники",
}
const tovar_home={
  name_1:"Домашний товар",
  name_2:"Радио",
  name_3:"Клавиатура",
  name_4:"Мышка",
  name_5:"Флешка"
}
const tovar_komplek={
  name_1:"Комплектующие",
  name_2:"Процессоры",
  name_3:"Модули памяти",
  name_4:"Видеокарты",
  name_5:"Звуковые карты"
}
</script>
<style>
.item-error{
padding: 0;
margin: 0;
}
.frum{
  padding-top: 4em;
  margin-top: 5em;
}
.item-fruit{
  margin-top: 3em;
  padding-top: 3em;
}
.modal-contentб,.modal-dialog,.modal-content{
  padding-left: 15em;
}
.col-md-6{
  gap: 3em;
}
</style>
<template>
    <header>
<div class="header-main">

  <div class="container">

    <a href="#" class="header-logo">
      <img src="../assets/Logo-hotech.png" alt="HiTech" >
    </a>

    <div class="header-search-container">


      <input type="search" name="search" v-model="input"  class="search-field" placeholder="Найди свою технику...">

      <div class="item-fruit" v-for="fruit in filteredList()" :key="fruit">
      <p class="frum">{{ fruit }}</p>
    </div>
  <div class="item-error" v-if="input&&!filteredList().length">
     <p>No results found!</p>
  </div>

    

    </div>

    <div class="header-user-actions">

      <!--Modal-->
      <button class="action-btn" data-bs-toggle="modal" data-bs-target="#staticBackdrop">
        <ion-icon name="person-outline"></ion-icon>
      </button>
      
<!-- Modal -->
<div class="modal fade grow " id="staticBackdrop" data-bs-backdrop="static" data-bs-keyboard="false" tabindex="-1" aria-labelledby="staticBackdropLabel" aria-hidden="true">
  <div class="modal-dialog">
    <div class="modal-content">
      <div class="modal-header">
        <h1 class="modal-title fs-5" id="staticBackdropLabel">Регистрация</h1>
        <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
      </div>
      <div class="modal-body">
        <form class="row g-3">
  <div class="col-md-6">
    <label for="inputEmail4" class="form-label">Эл. адрес</label>
    <input type="email" class="form-control" id="inputEmail4">
  </div>
  <div class="col-md-6">
    <label for="inputPassword4" class="form-label">Пароль</label>
    <input type="password" class="form-control" id="inputPassword4">
  </div>
  <div class="col-12">
    <label for="inputAddress" class="form-label">Адрес</label>
    <input type="text" class="form-control" id="inputAddress" placeholder="Проспект Ленина">
  </div>
 
  <div class="col-md-6">
    <label for="inputCity" class="form-label">Город</label>
    <input type="text" class="form-control" id="inputCity" placeholder="Брянск">
  </div>
  <div class="col-md-4">
    <label for="inputState" class="form-label">Область</label>
    <select id="inputState" class="form-select">
      <option selected>Выберите...</option>
      <option>Тирасполь</option>
      <option>Бендеры</option>
    </select>
  </div>
 
  <div class="col-12">
    <div class="form-check">
      <input class="form-check-input" type="checkbox" id="gridCheck">
      <label class="form-check-label" for="gridCheck">
        Проверить меня
      </label>
    </div>
  </div>
 
</form>
      </div>
      <div class="modal-footer">
        <button type="button" class="btn-secondary" data-bs-dismiss="modal">Закрыть</button>
        <button type="button" class=" btn-primary">Отправить</button>
      </div>
    </div>
  </div>
</div>
   

    </div>

  </div>

</div>

<nav class="desktop-navigation-menu">

  <div class="container">

    <ul class="desktop-menu-category-list">

      <li class="menu-category">
        <a href="#" class="menu-title">Главное</a>
      </li>

      <li class="menu-category">
        <a href="#" class="menu-title"></a>

        <div class="dropdown-panel">

          <ul class="dropdown-panel-list">

            <li class="menu-title">
              <a href="#">{{tovar_bitovaya_tehnika.name_1}}</a>
            </li>

            <li class="panel-list-item">
              <a href="#">Компьютеры</a>
            </li>

            <li class="panel-list-item">
              <a href="#">{{tovar_bitovaya_tehnika.name_2}}</a>
            </li>

            <li class="panel-list-item">
              <a href="#">{{tovar_bitovaya_tehnika.name_3}}</a>
            </li>

            <li class="panel-list-item">
              <a href="#">{{tovar_bitovaya_tehnika.name_4}}</a>
            </li>

            <li class="panel-list-item">
              <a href="#">{{tovar_bitovaya_tehnika.name_5}}</a>
            </li>

            <li class="panel-list-item">
              <a href="#">
                <img src="https://img.joomcdn.net/9c967a2a4ba28a2019fc4a02bd6ccd824662557b_original.jpeg" alt="headphone collection" width="250"
                  height="119">
              </a>
            </li>

          </ul>

          <ul class="dropdown-panel-list">

            <li class="menu-title">
              <a href="#">{{ tovar_PC.name_1 }}</a>
            </li>

            <li class="panel-list-item">
              <a href="#">{{ tovar_PC.name_2 }}</a>
            </li>

            <li class="panel-list-item">
              <a href="#">{{ tovar_PC.name_3 }}</a>
            </li>

            <li class="panel-list-item">
              <a href="#">{{ tovar_PC.name_4 }}</a>
            </li>

            <li class="panel-list-item">
              <a href="#">{{ tovar_PC.name_5 }}</a>
            </li>

           

            <li class="panel-list-item">
              <a href="#">
                <img src="https://img.joomcdn.net/9c967a2a4ba28a2019fc4a02bd6ccd824662557b_original.jpeg" alt="men's fashion" width="250" height="119">
              </a>
            </li>

          </ul>

          <ul class="dropdown-panel-list">

            <li class="menu-title">
              <a href="#">{{ tovar_home.name_1 }}</a>
            </li>

            <li class="panel-list-item">
              <a href="#">{{tovar_home.name_2}}</a>
            </li>

            <li class="panel-list-item">
              <a href="#">{{tovar_home.name_3}}</a>
            </li>

            <li class="panel-list-item">
              <a href="#">{{tovar_home.name_4}}</a>
            </li>

            <li class="panel-list-item">
              <a href="#">{{tovar_home.name_5}}</a>
            </li>

            

            <li class="panel-list-item">
              <a href="#">
                <img src="https://img.joomcdn.net/f3cfa746fdb062e5dc4b2f9ca052e30fecba2d5a_original.jpeg" alt="tovar" width="250" height="119">
              </a>
            </li>

          </ul>

         

        </div>
      </li>

      <li class="menu-category">
        <a href="#" class="menu-title">{{tovar_PC.name_1}}</a>

        <ul class="dropdown-list">

          <li class="dropdown-item">
            <a href="#">{{tovar_PC.name_2}}</a>
          </li>

          <li class="dropdown-item">
            <a href="#">{{tovar_PC.name_3}}</a>
          </li>

          <li class="dropdown-item">
            <a href="#">{{tovar_PC.name_4}}</a>
          </li>

          <li class="dropdown-item">
            <a href="#">{{tovar_PC.name_5}}</a>
          </li>

        </ul>
      </li>

      <li class="menu-category">
        <a href="#" class="menu-title">{{tovar_home.name_1}}</a>

        <ul class="dropdown-list">

          <li class="dropdown-item">
            <a href="#">{{tovar_home.name_2}}</a>
          </li>

          <li class="dropdown-item">
            <a href="#">{{tovar_home.name_3}}</a>
          </li>

          <li class="dropdown-item">
            <a href="#">{{tovar_home.name_4}}</a>
          </li>

          <li class="dropdown-item">
            <a href="#">{{tovar_home.name_5}}</a>
          </li>

        </ul>
      </li>

      <li class="menu-category">
        <a href="#" class="menu-title">{{ tovar_bitovaya_tehnika.name_1}}</a>

        <ul class="dropdown-list">

          <li class="dropdown-item">
            <a href="#">{{ tovar_bitovaya_tehnika.name_2}}</a>
          </li>

          <li class="dropdown-item">
            <a href="#">{{ tovar_bitovaya_tehnika.name_3}}</a>
          </li>

          <li class="dropdown-item">
            <a href="#">{{ tovar_bitovaya_tehnika.name_4}}</a>
          </li>

          <li class="dropdown-item">
            <a href="#">{{ tovar_bitovaya_tehnika.name_5}}</a>
          </li>

        </ul>
      </li>

      <li class="menu-category">
        <a href="#" class="menu-title">{{ tovar_komplek.name_1}}</a>

        <ul class="dropdown-list">

          <li class="dropdown-item">
            <a href="#">{{  tovar_komplek.name_2 }}</a>
          </li>

          <li class="dropdown-item">
            <a href="#">{{  tovar_komplek.name_3 }}</a>
          </li>

          <li class="dropdown-item">
            <a href="#">{{  tovar_komplek.name_4  }}</a>
          </li>

          <li class="dropdown-item">
            <a href="#">{{  tovar_komplek.name_5 }}</a>
          </li>

        </ul>
      </li>

      <li class="menu-category">
        <a href="#" class="menu-title">Новости</a>
      </li>

      <li class="menu-category">
        <a href="#" class="menu-title">Контакты</a>
      </li>

    </ul>

  </div>

</nav>




</header>

</template>

<style scoped>
@import '../assets/main.css';
</style>

