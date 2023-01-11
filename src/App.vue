<template>
  <Navigation/>
  <Products/>
  <Footer/>
</template>

<script>
import Navigation from "@/components/page/Navigation";
import Products from "@/components/page/Products";
import Footer from "@/components/page/Footer";
export default {
  name: 'App',
  components: {
    Navigation,
    Products,
    Footer
  }
}
</script>

<style>
    @import './assets/css/App.css';
</style>
