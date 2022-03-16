<template>
  <article class="product">
        <img :src="require('../assets/images/products/' + product.image)" alt="" class="product__preview">
        <span class="product__price">{{ product.price }} ₽</span>
        <h4 class="product__name">{{ product.name.slice(0, 30) + '...' }}</h4>
        <div class="product__footer">
            <v-switcher />
            <button class="product__cart-btn">В корзину</button>
        </div>
    </article>
</template>

<script>
import vSwitcher from '@/components/v-switcher.vue'

export default {
    props: {
        product: Object
    },

    components: {
        vSwitcher
    }
}
</script>

<style scoped>

.product {
    margin: 10px;
    width: calc(25% - 20px);
    background-color: #fff;
    padding: 30px 20px;
    border-radius: 20px;
}

.product__preview {
    width: 100%;
    height: auto;
}

.product__price {
    font-size: 18px;
    line-height: 24px;
    color: #000;
    font-weight: 700;
    margin-right: 10px;
}

.product__name {
    font-size: 14px;
    line-height: 20px;
    color: #999;
    font-weight: 400;
}

.product__footer {
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: space-between;
}

.product__cart-btn {
    padding: 10px 20px;
    color: #fff;
    background-color: #b30f97;
    border: none;
    border-radius: 12px;
    font-weight: 700;
    cursor: pointer;
}

.product__cart-btn:hover {
    background-color: #e313bf;
}
</style>