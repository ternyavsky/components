<script setup lang="ts">
import { defineEmits, defineProps } from "vue";

const props = defineProps<{
  isOpen: boolean;
  title: string;
  description: string;
  img: string;
}>();

const emit = defineEmits<{
  toggle: [];
}>();

const handleToggle = () => {
  emit("toggle");
};
</script>
<template>
  <div class="about-drop__header">
    <img
      :src="img"
      alt="drop-header-icon"
      class="about-drop__header__icon about-drop__header__icon--desktop"
    />
    <img
      :src="img"
      alt="drop-header-icon"
      class="about-drop__header__icon about-drop__header__icon--mobile"
    />
    <div class="about-drop__header__info">
      <div class="about-drop__header__text">
        <h2 class="about-drop__header__title">{{ title }}</h2>
        <p class="about-drop__header__description">{{ description }}</p>
      </div>
      <div class="about-drop__header__button" @click="handleToggle">
        <img
          src="/src/assets/arrow-up.svg"
          alt="arrow-right"
          class="about-drop__header__button-icon"
          :class="{ 'about-drop__header__button-icon--rotated': !props.isOpen }"
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

  @media (max-width: @laptop) {
    gap: 24px;
    padding: 14px 0px 14px 14px;
    border-radius: 28px;
  }

  @media (max-width: @tablet) {
    gap: 20px;
    padding: 12px 0px 12px 12px;
    border-radius: 24px;
  }

  @media (max-width: @mobile) {
    border-radius: 20px;
    padding: 8px 0px 8px 8px;
    gap: 12px;
    margin: 0px 16px;
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

    @media (max-width: @laptop) {
      padding-right: 28px;
      gap: 24px;
    }

    @media (max-width: @tablet) {
      padding-right: 24px;
      gap: 20px;
    }

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
    transition: transform 0.3s ease;

    @media (max-width: @laptop) {
      width: 44px;
      height: 44px;
      border-radius: 12px;
      padding: 16px 13px;
    }

    @media (max-width: @tablet) {
      width: 36px;
      height: 36px;
      border-radius: 10px;
      padding: 12px 10px;
    }

    @media (max-width: @mobile) {
      width: 24px;
      height: 24px;
      border-radius: 24px;
      padding: 5px;
    }

    &--rotated {
      transform: rotate(180deg);
    }
  }
  &__icon {
    border-radius: 20px;
    width: 232px;
    height: 88px;
    object-fit: cover;
    flex-shrink: 0;

    @media (max-width: @laptop) {
      width: 200px;
      height: 76px;
      border-radius: 18px;
    }

    @media (max-width: @tablet) {
      width: 150px;
      height: 60px;
      border-radius: 16px;
    }

    @media (max-width: @mobile) {
      width: 80px;
      height: 48px;
      border-radius: 12px;
    }

    &--desktop {
      display: block;
      @media (max-width: @tablet) {
        display: none;
      }
    }

    &--mobile {
      display: none;
      @media (max-width: @tablet) {
        display: block;
      }
    }
  }

  &__title {
    font-size: 1.75rem;
    font-weight: 900;
    line-height: 44px;

    @media (max-width: @laptop) {
      font-size: 1.5rem;
      line-height: 36px;
    }

    @media (max-width: @tablet) {
      font-size: 1.25rem;
      line-height: 30px;
    }

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

    @media (max-width: @laptop) {
      font-size: 1.125rem;
      line-height: 26px;
    }

    @media (max-width: @tablet) {
      font-size: 1rem;
      line-height: 22px;
    }

    @media (max-width: @mobile) {
      font-size: 0.875rem;
      line-height: 16px;
      font-weight: 600;
    }
  }
}
</style>
