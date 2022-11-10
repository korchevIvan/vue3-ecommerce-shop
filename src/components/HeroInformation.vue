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
    <Button :color="colorLink" type="link" to="/">
      View collection
    </Button>
  </div>
</template>

<script setup>
import Button from '@/components/UI/Button.vue'

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
    default: 'secondary'
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
    align-items: flex-start;
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
  }
}
</style>