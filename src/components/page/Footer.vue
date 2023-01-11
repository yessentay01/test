<template>
  <section class="footer">
    <div class="container footer__content">
      <div class="footer__menu">
        <a href="#"><img src="../../assets/images/logo.png" width="48" alt=""></a>
        <a href="#" class="footer__menu-link">Каталог</a>
        <a href="#" class="footer__menu-link">Доставка</a>
        <a href="#" class="footer__menu-link">Оплата</a>
        <a href="#" class="footer__menu-link">Контакты</a>
        <a href="#" class="footer__menu-link">О галерее</a>
      </div>
      <div>
        <a href="tel:774955555555" class="footer__menu-link">+7 (495) 555-55-55</a>
        <a href="#" class="footer__menu-link">г. Москва, ул. Расплетина, 24</a>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Footer"
}
</script>

<style scoped>
  .footer{
    background: #ECEAEA;
    position:fixed;
    bottom:0;
    right: 0;
    left: 0;
  }
  .footer__content{
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  .footer__menu{
    display: flex;
    align-items: center;
    margin:24px 0;
  }
  .footer__menu-link{
    font-weight: 40;
    font-size: 14px;
    color: #555555;
    text-decoration: none;
    margin-left: 48px;
  }

</style>