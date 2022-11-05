<template>
  <div class="product">
    <a href="#">
      <img :src="img" :alt="title" class="product-image">
    </a>
    <a href="#" class="product-name">{{ title }}</a>
    <span class="product-price">
      £{{ price }}
    </span>
  </div>
</template>

<script setup>
const props = defineProps({
  img: {
    type: String,
    required: true
  },
  title: {
    type: String,
    required: true
  },
  price: {
    type: Number,
    required: true
  },

})
</script>

<style lang="scss" scoped>
.product {
  &-image {
    display: block;
    margin-bottom: 24px;
  }

  &-name {
    font-family: 'Clash Display', sans-serif;
    display: block;
    color: #2A254B;
    font-weight: 400;
    font-size: 20px;
    line-height: 1.4;
    margin-bottom: 8px;
    text-decoration: none;

    &:hover {
      text-decoration-skip-ink: none;
      text-decoration: underline;
    }
  }

  &-price {
    color: #2A254B;
    font-size: 18px;
    line-height: 1.5;
  }
}
</style>