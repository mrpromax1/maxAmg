<template>
  <header>
    <div class="container">
      <div class="header">
        <a href="#" class="header__logo">
          <img src="./assets/images/logo.svg" alt="logo">
        </a>
        <div class="search header__search">
          <input type="text" class="search__input" placeholder="Я ищу...">
          <button class="search__btn"></button>
        </div>

        <v-cart />
        
      </div>
    </div>
  </header>

  <main class="main">
    <div class="container">
      <section class="products">
        <div class="products__head">
          <span class="products__amount">3 899 товаров</span>
          <div class="products__view">
            <button class="product__view-btn product__view-btn--large product__view-btn--active"></button>
            <button class="product__view-btn product__view-btn--small"></button>
          </div>
        </div>

        <div class="products__list">
          <v-product 
            v-for="product in products"
            :key="product.vendorCode"
            :product="product"
          />
        </div>

        <div class="pagination">
          <ul class="pagination__list">
            <li class="pagination__item pagination__item--active">1</li>
            <li class="pagination__item">2</li>
            <li class="pagination__item">3</li>
            <li class="pagination__item">4</li>
            <li class="pagination__item">5</li>
            <li class="pagination__item">6</li>
            <li class="pagination__item">7</li>
          </ul>
        </div>
      </section>
    </div>
  </main>

  <footer>
    <div class="container">
      <div class="footer">
        <p class="footer__copyright">
          2004-2022 &copy; Wildberries — модный интернет-магазин одежды, обуви и аксессуаров. <br> Все права защищены. Доставка по всей России.
        </p>
      </div>
    </div>
  </footer>
</template>

<script>
import vCart from '@/components/v-cart.vue'
import vProduct from '@/components/v-product.vue'

export default {
  components: {
    vCart,
    vProduct
  },

  data() {
    return {
      products: [
        { name: 'кеды Air Force 1 "07 LX', image: '1.webp', price: 11301, vendorCode: 'A1' },
        { name: 'кроссовки Air Alpha Force Premium Albis Pack', image: '2.jpg', price: 7899, vendorCode: 'A2' },
        { name: 'кроссовки Air Force 1 "07', image: '3.webp', price: 6777, vendorCode: 'A3' },
        { name: 'кроссовки Air Force 1 "07 LV8', image: '4.webp', price: 9299, vendorCode: 'A4' },
        { name: 'кроссовки Dunk Low Retro', image: '5.webp', price: 14600, vendorCode: 'A5' },
      ]
    }
  }

}
</script>

<style src="./assets/styles/index.css"></style>
