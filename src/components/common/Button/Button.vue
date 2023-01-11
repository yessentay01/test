<template>
    <button :class="type"  v-html="text" :disabled="type === 'basket'"/>
</template>

<script>
import PulseLoader from 'vue-spinner/src/PulseLoader.vue'

export default {
  name: "Button",
  components:{
    PulseLoader
  },
  props: {
    text: String,
    type: String,
  },
  data() {
    return {
      inBasket: false,
    }
  },

}
</script>

<style scoped>
  button{
    color: #fff;
    border: none;
    font-size: 14px;

  }
  button:hover{
    background: #776763;
  }
  .search{
    padding: 13px 36px 14px 36px;
    background: #403432;
    cursor: pointer;
  }
  .default{
    padding: 14px 30px 13px 30px;
    background: #382E2B;
    cursor: pointer;
  }
  .basket{
    padding: 14px 30px 13px 30px;
    background: #5B3A32;
    cursor: default;
  }
</style>