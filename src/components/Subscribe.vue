<template>
  <div class="subscribe">
    <div class="subscribe-content">
      <h3 class="subscribe-title">Join the club and get the benefits</h3>
      <span class="subscribe-description">
        Sign up for our newsletter and receive exclusive offers on new ranges, sales, pop up stores and more
      </span>
      <div class="subscribe-checks">
        <div class="subscribe-check">
          <img src="/svg/check.svg" alt="check" class="subscribe-check__icon">
          <span class="subscribe-check__name">
            Exclusive offers
          </span>
        </div>
        <div class="subscribe-check">
          <img src="/svg/check.svg" alt="check" class="subscribe-check__icon">
          <span class="subscribe-check__name">
            Free events
          </span>
        </div>
        <div class="subscribe-check">
          <img src="/svg/check.svg" alt="check" class="subscribe-check__icon">
          <span class="subscribe-check__name">
            Large discounts
          </span>
        </div>
      </div>
      <SubscribeForm/>
    </div>
  </div>
</template>

<script setup>
import SubscribeForm from '@/components/SubscribeForm.vue'
</script>

<style lang="scss" scoped>
.subscribe {
  background-image: url('/img/subscribe.jpg');
  background-size: cover;
  padding: 97px 0 86px;

  &-content {
    max-width: 500px;
    margin: auto;
    text-align: center;
    color: #FFF;
  }

  &-title {
    margin: 0 0 12px;
    font-size: 32px;
    font-weight: 400;
    font-family: var(--clash);
  }

  &-description {
    display: block;
    font-size: 18px;
    margin-bottom: 30px;
  }

  &-checks {
    display: flex;
    justify-content: center;
    margin-bottom: 40px;
  }
  &-check {
    display: flex;
    align-items: center;
    &:nth-child(2) {
      margin: 0 36px;
    }
    &__icon {
      margin-right: 9px;
    }
  }
}
</style>