<template>
  <form class="subscribe-form">
    <input
        type="text"
        class="input-text subscribe-form__input"
        placeholder="your@email.com"
        :style="
        {backgroundColor: bgInput, color: colorText}"
    >
    <Button :color="colorButton || 'primary'">Sign Up</Button>
  </form>
</template>

<script setup>
import Button from '@/components/UI/Button.vue'

const props = defineProps({
  bgInput: {
    type: String,
    required: false
  },
  colorButton: {
    type: String,
    required: false
  },
  colorText: {
    type: String,
    required: false
  }
})
</script>

<style lang="scss">
.subscribe-form {
  display: flex;
  &__input {
    flex-grow: 1;
  }
}
</style>