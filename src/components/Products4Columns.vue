<template>
  <div class="products-container">
    <div class="products">
      <Product
          v-for="product in products"
          :key="product.id"
          :img="product.img"
          :title="product.title"
          :price="product.price"
      />
    </div>
    <router-link to="#" class="products-link">View collection</router-link>
  </div>
</template>

<script setup>
import {ref} from "vue"
import Product from '@/components/Product.vue'

const products = ref([
  {
    id: 1,
    img: '/img/product1.jpg',
    title: 'The Dandy chair',
    price: 250,
  },
  {
    id: 2,
    img: '/img/product2.jpg',
    title: 'Rustic Vase Set',
    price: 155,
  },
  {
    id: 3,
    img: '/img/product3.jpg',
    title: 'The Silky Vase',
    price: 125,
  },
  {
    id: 4,
    img: '/img/product4.jpg',
    title: 'The Lucy Lamp',
    price: 399,
  },
])
</script>

<style lang="scss" scoped>

.products {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  column-gap: 20px;
  padding: 0 80px;
  margin-bottom: 64px;
  &-container {
    margin-bottom: 56px;
  }
  &-link {
    text-align: center;
    display: block;
    font-weight: 400;
    font-size: 16px;
    line-height: 1.5;
    color: var(--black);
    text-decoration: none;
    &:hover {
      text-decoration-skip-ink: none;
      text-decoration: underline;
    }
  }
}

</style>