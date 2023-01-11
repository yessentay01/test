<template>
  <div class="navigation">
    <div class="container navigation__content">
      <div class="navigation__menu">
        <a href="#"><img src="../../assets/images/logo.png" width="48" alt=""></a>
        <a href="#" class="navigation__menu-link">Каталог</a>
        <a href="#" class="navigation__menu-link">Доставка</a>
        <a href="#" class="navigation__menu-link">Оплата</a>
        <a href="#" class="navigation__menu-link">Контакты</a>
        <a href="#" class="navigation__menu-link">О галерее</a>
      </div>
      <div class="navigation__search">
        <form action="#">
          <input type="text" class="navigation__search-input" placeholder="Поиск по названию картины">
          <Button text="Найти" type="search"/>
        </form>
      </div>
    </div>
  </div>
</template>

<script>
import Button from "@/components/common/Button/Button";
export default {
  name: "NavigationMenu",
  components:{
    Button
  }
}
</script>

<style scoped>
  .navigation{
    border-bottom: 1px solid #E1E1E1;
  }
  .navigation__content{
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .navigation__menu{
    display: flex;
    align-items: center;
    margin:24px 0;
  }
  .navigation__menu-link{
    font-weight: 40;
    font-size: 14px;
    color: #343030;
    text-decoration: none;
    margin-left: 48px;
  }
  .navigation__search-input{
    width: 294px;
    color: #343030;
    border: 1px solid #E1E1E1;
    padding: 13px 16px 14px 16px;
  }
  .navigation__search-input::placeholder{
    color: #9F9F9F;
    font-weight: 400;
    font-size: 14px;
  }
  .navigation__search-input:focus{
    outline: none;
    border: 1px solid #B5B5B5;
  }
</style>