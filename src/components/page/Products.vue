<template>
  <section class="products">
    <div class="container">
      <h1 class="products__title">Картины эпохи Возрождения</h1>
      <div class="products__content">
        <Item v-for="item in items" :key="item.id" :item="item" />
      </div>
    </div>
  </section>
</template>

<script>
import Item from "@/components/common/Item/Item";
export default {
  name: "Products",
  components: {
    Item
  },
  data() {
    return {
      items: [
        {
          id: 1,
          img: require('../../assets/images/Item/item1.png'),
          title: '«Рождение Венеры» Сандро Боттичелли',
          old_price: '2 000 000 $',
          price: '1 000 000 $'
        },
        {
          id: 2,
          img: require('../../assets/images/Item/item2.png'),
          title: '«Тайная вечеря»  Леонардо да Винчи',
          old_price: false,
          price: '3 000 000 $'
        },
        {
          id: 3,
          img: require('../../assets/images/Item/item3.png'),
          title: '«Сотворение Адама» Микеланджело',
          old_price: '6 000 000 $',
          price: '5 000 000 $'

        },
        {
          id: 4,
          img: require('../../assets/images/Item/item4.png'),
          title: '«Урок анатомии»  Рембрандт',
          old_price: false,
          price: false
        },
      ],
    }
  },

}
</script>

<style scoped>
  .products__title{
    font-style: normal;
    font-weight: 700;
    font-size: 24px;
    line-height: 36px;
    padding: 45px 0 40px 0;
    margin: 0;
  }
  .products__content{
    display: flex;
    justify-content: space-between;
  }
</style>