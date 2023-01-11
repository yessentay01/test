<template>
    <div class="item" :class="{ item__sold: !item.price }">
      <img  :src="item.img" class="item__image"  alt="">
      <h2 class="item__title" v-text="item.title"></h2>
      <div class="item__bottom">
        <div class="item__price-container" >
          <h5 class="item__old-price" v-if="item.old_price" v-text="item.old_price"></h5>
          <h3 class="item__price" v-if="item.price" v-text="item.price"></h3>
          <h4 v-if="!item.price">Продана на аукционе</h4>
        </div>
        <Button v-if="item.price" :text="text" @click="addToBasket(item.id)" :type="type" />
      </div>
    </div>
</template>

<script>
import Button from "@/components/common/Button/Button";
import PulseLoader from 'vue-spinner/src/PulseLoader.vue'

export default {
  name: "Item",
  props:{
    item: Object
  },
  components: {
    Button,
    PulseLoader
  },
  data() {
    return {
      text:'Купить',
      type:'default',
    }
  },
  methods: {
    async addToBasket(id){
      this.text='Загрузка'
      await this.axios.get(`https://jsonplaceholder.typicode.com/posts/${id}`).then((response) => {
        console.log(12);
        console.log(response.data)
        this.text = "В корзине"
        this.type = "basket"
      })
    }
  }


}
</script>

<style scoped>
  .item{
    width: 280px;
    border: 1px solid #E1E1E1;
  }
  .item__title{
    font-style: normal;
    font-weight: 400;
    font-size: 18px;
    line-height: 27px;
    color: #343030;
    padding: 0 24px;
    margin: 20px 0 0 0;
  }
  .item__bottom{
    display: flex;
    justify-content: space-between;
    padding: 24px;
  }
  .item__old-price{
    margin: 0;
    padding: 0;
    text-decoration: line-through;
    color: #A0A0A0;
    font-weight: 300;
    font-size: 14px;
    line-height: 21px;
  }
  .item__price{
    margin: 0;
    padding: 0;
    font-style: normal;
    font-weight: 700;
    font-size: 16px;
    color: #343030;
    line-height: 24px;
  }
  .item__price-container{
    align-self: center;
  }
  .item__sold{
    opacity: 0.6;
  }
</style>