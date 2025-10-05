<script setup lang="ts"></script>
<template>
  <div class="about-drop__header">
    <img
      src="/src/assets/mirror-girl.svg"
      alt="drop-header-icon"
      class="about-drop__header__icon about-drop__header__icon--desktop"
    />
    <img
      src="/src/assets/mobile-mirror-girl.svg"
      alt="drop-header-icon"
      class="about-drop__header__icon about-drop__header__icon--mobile"
    />
    <div class="about-drop__header__info">
      <div class="about-drop__header__text">
        <h2 class="about-drop__header__title">Личные качества</h2>
        <p class="about-drop__header__description">Плюсы и минусы</p>
      </div>
      <div class="about-drop__header__button">
        <img
          src="/src/assets/arrow-up.svg"
          alt="arrow-right"
          class="about-drop__header__button-icon"
        />
      </div>
    </div>
  </div>
</template>

<style lang="less" scoped>
@import "../styles/variables.less";
.about-drop__header {
  display: flex;
  flex-direction: row;
  align-items: center;
  gap: 28px;
  background-color: @color-header-bg;
  padding: 16px 0px 16px 16px;
  border-radius: 32px;
  @media (max-width: @mobile) {
    border-radius: 20px;
    padding: 8px 0px 8px 8px;
    gap: 12px;
  }
  &__info {
    display: flex;
    justify-content: space-between;
    width: 100%;
  }
  &__text {
    display: flex;
    flex-direction: column;
    justify-content: center;
    color: @color-default-bg;
  }
  &__button {
    display: flex;
    flex-direction: row;
    align-items: center;
    padding-right: 32px;
    cursor: pointer;
    gap: 28px;
    @media (max-width: @mobile) {
      padding-right: 16px;
    }
  }
  &__button-icon {
    width: 48px;
    height: 48px;
    border-radius: 14px;
    padding: 18px 15px;
    background: @color-default-bg;
    @media (max-width: @mobile) {
      width: 24px;
      height: 24px;
      border-radius: 24px;
      padding: 5px;
    }
  }
  &__icon {
    border-radius: 20px;
    max-width: 232px;
    max-height: 88px;
    object-fit: contain;
    width: 100%;
    height: 100%;
    @media (max-width: @mobile) {
      max-width: 73px;
      min-height: 48px;
      border-radius: 12px;
    }

    &--desktop {
      display: block;
      @media (max-width: @mobile) {
        display: none;
      }
    }

    &--mobile {
      display: none;
      @media (max-width: @mobile) {
        display: block;
      }
    }
  }
  &__title {
    font-size: 1.75rem;
    font-weight: 900;
    line-height: 44px;
    @media (max-width: @mobile) {
      font-size: 1.125rem;
      line-height: 24px;
      font-weight: 800;
    }
  }
  &__description {
    font-size: 1.25rem;
    font-weight: 400;
    line-height: 28px;
    @media (max-width: @mobile) {
      font-size: 0.875rem;
      line-height: 16px;
      font-weight: 600;
    }
  }
}
</style>
