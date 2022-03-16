<template>
  <div class="cart">
        <button class="cart__btn" @click="cartVisible = !cartVisible">
            <i class="cart__btn-icon">
                <div class="cart__amount">1</div>
            </i>
            <span class="cart__btn-label">Корзина</span>
        </button>

        <div class="cart__list" v-if="cartVisible">
            <div class="cart-item">
                <img src="../assets/images/products/1.webp" alt="" class="cart-item__preview">
                <span class="cart-item__name">кеды Air Force 1 '07 LX</span>
                <v-switcher />
                <span class="cart-item__price">11 301 ₽</span>
                <a href="#" class="cart-item__remove">Удалить</a>
            </div>
        </div>
    </div>
</template>

<script>
import vSwitcher from '@/components/v-switcher.vue'

export default {
    components: {
        vSwitcher
    },
    data() {
        return {
            cartVisible: false
        }
    }
}
</script>

<style>

</style>