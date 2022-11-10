<template>
  <div
      class="hero-info"
      :style="{background: background}"
  >
    <div class="hero-info-text">
      <h2
          class="hero-info__title" v-if="title"
          :style="{color: colorTitle}"
      >
        {{title}}
      </h2>
      <span
          class="hero-info__description"
          :style="{color: colorDescription}"
          v-if="description"
      >
        {{description}}
      </span>
    </div>
    <router-link
        :to="link"
        class="hero-info-link"
        v-if="link"
        :style="{color: colorLink}"
    >
      View collection
    </router-link>
  </div>
</template>

<script setup>
const props = defineProps({
  title: {
    type: String,
    required: false
  },
  description: {
    type: String,
    required: false
  },
  link: {
    type: String,
    required: false
  },
  colorTitle: {
    type: String,
    default: ''
  },
  colorDescription: {
    type: String,
    default: '#5B5676'
  },
  colorLink: {
    type: String,
    default: '#2A254B'
  },
  background: {
    type: String,
    default: ''
  },

})

</script>

<style lang="scss" scoped>
.hero {
  &-info {
    max-width: 630px;
    background: #FFF;
    padding: 50px 55px;
    min-height: 444px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;

    &__title {
      font-family:var(--clash);
      font-weight: 400;
      font-size: 32px;
      line-height: 1.4;
      margin: 0 0 20px;
    }
    &__description {
      font-size: 18px;
      line-height: 1.5;
    }
    &-link {
      text-decoration: none;
      width: 170px;
      height: 56px;
      display: flex;
      align-items: center;
      justify-content: center;
      background: rgba(249, 249, 249, 0.15);
      &:hover {
        background: rgba(249, 249, 249, 0.30);
      }
    }
  }
}
</style>