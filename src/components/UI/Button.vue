<template>
  <button
      :class="['btn', {
          'btn--primary': color === 'primary',
          'btn--secondary': color === 'secondary',
          'btn--light-gray': color === 'light-gray',
          'btn--white': color === 'white'
      }]"
      :style="{backgroundColor: background}"
      v-if="type === 'button'"
  >
    <slot/>
  </button>
  <router-link
      v-else
      :to="to"
      :class="['btn', {
          'btn--primary': color === 'primary',
          'btn--secondary': color === 'secondary',
          'btn--light-gray': color === 'light-gray'
      }]"
      :style="{backgroundColor: background}"
  >
    <slot/>
  </router-link>
</template>

<script setup>
const props = defineProps({
  background: {
    type: String,
    required: false,
  },
  type: {
    type: String,
    default: 'button'
  },
  to: {
    type: String,
    required: false
  },
  color: {
    type: String,
    default: 'primary'
  }
})
</script>

<style lang="scss" scoped>

.btn {
  background: var(--dark-primary);
  color: #FFF;
  padding: 0 32px;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
  border: none;
  font-size: 16px;
  height: 56px;
  text-decoration: none;

  &:hover {
    opacity: .8;
  }

  //text-decoration: none;
  //width: 170px;
  //height: 56px;
  //display: flex;
  //align-items: center;
  //background: rgba(249, 249, 249, 0.15);
  //
  //&:hover {
  //  background: rgba(249, 249, 249, 0.30);
  //}

  &--primary {
    background: var(--dark-primary);
    color: #FFF;
  }

  &--secondary {
    background: rgba(249, 249, 249, 0.15);
    color: #FFF;
  }

  &--light-gray {
    background: var(--light-gray);
    color: #2A254B;
  }
  &--white {
    background: #FFF;
    color: var(--dark-primary);
  }
}

</style>