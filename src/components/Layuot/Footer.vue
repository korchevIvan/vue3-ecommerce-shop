<template>
  <footer class="footer">
    <div class="footer-content">
      <div class="footer-top">
        <div class="footer-menu">
          <div class="footer-menu-column">
            <span class="footer-menu__title">
              Menu
            </span>
            <router-link to="#" class="footer-menu__link">New arrivals</router-link>
            <router-link to="#" class="footer-menu__link">Best sellers</router-link>
            <router-link to="#" class="footer-menu__link">Recently viewed</router-link>
            <router-link to="#" class="footer-menu__link">Popular this week</router-link>
            <router-link to="#" class="footer-menu__link">All products</router-link>
          </div>
          <div class="footer-menu-column">
            <span class="footer-menu__title">
              Categories
            </span>
            <router-link to="#" class="footer-menu__link">Crockery</router-link>
            <router-link to="#" class="footer-menu__link">Furniture</router-link>
            <router-link to="#" class="footer-menu__link">Homeware</router-link>
            <router-link to="#" class="footer-menu__link">Plant pots</router-link>
            <router-link to="#" class="footer-menu__link">Chairs</router-link>
            <router-link to="#" class="footer-menu__link">Crockery</router-link>
          </div>
          <div class="footer-menu-column">
            <span class="footer-menu__title">
              Our company
            </span>
            <router-link to="#" class="footer-menu__link">About us</router-link>
            <router-link to="#" class="footer-menu__link">Vacancies</router-link>
            <router-link to="#" class="footer-menu__link">Contact us</router-link>
            <router-link to="#" class="footer-menu__link">Privacy</router-link>
            <router-link to="#" class="footer-menu__link">Returns policy</router-link>
          </div>
        </div>
        <div class="footer-subscribe">
          <SubscribeForm
              color-button="white"
              bg-input="rgba(255, 255, 255, 0.15)"
              color-text="#FFF"
          />
        </div>
      </div>
      <div class="footer-bottom">
        <span class="footer-bottom__copy">
          Copyright 2022 Avion LTD
        </span>
        <div class="footer-bottom__socials">
          <a href="#" class="footer-bottom__socials__link">
            <img src="/svg/linkedin.svg" alt="linkedin">
          </a>
          <a href="#" class="footer-bottom__socials__link">
            <img src="/svg/facebook.svg" alt="facebook">
          </a>
          <a href="#" class="footer-bottom__socials__link">
            <img src="/svg/instagram.svg" alt="instagram">
          </a>
          <a href="#" class="footer-bottom__socials__link">
            <img src="/svg/skype.svg" alt="skype">
          </a>
          <a href="#" class="footer-bottom__socials__link">
            <img src="/svg/twitter.svg" alt="twitter">
          </a>
          <a href="#" class="footer-bottom__socials__link">
            <img src="/svg/pinterest.svg" alt="pinterest">
          </a>

        </div>
      </div>
    </div>
  </footer>
</template>

<script setup>
import SubscribeForm from '@/components/SubscribeForm.vue'
</script>

<style lang="scss" scoped>
.footer {
  background: var(--dark-primary);
  color: #FFF;

  &-content {
    padding: 58px 82px 25px;
  }

  &-top {
    display: grid;
    grid-template-columns: 540px 1fr;
    column-gap: 110px;
    padding-bottom: 48px;
    border-bottom: 1px solid var(--primary);
  }
  &-menu {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    &__title {
      font-family: var(--clash);
      display: block;
      margin-bottom: 12px;
    }
    &__link {
      display: block;
      color: #FFF;
      font-size: 14px;
      text-decoration: none;
      text-decoration-skip-ink: none;
      margin-bottom: 12px;
      &:last-child {
        margin-bottom: 0;
      }
      &:hover {
        text-decoration: underline;
      }
    }
  }
  &-bottom {
    padding-top: 22px;
    display: flex;
    justify-content: space-between;
    &__copy {
      font-size: 14px;
    }
    &__socials {
      display: flex;
      align-items: center;
      &__link {
        margin: 0 12px;
        &:hover {
          opacity: 0.8;
        }
      }
    }
  }
}
</style>