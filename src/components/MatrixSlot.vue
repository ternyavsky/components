<script setup lang="ts">
defineProps<{
  title: string;
  description: string;
  img: string;
}>();
</script>
<template>
  <div class="matrix-slot">
    <div class="matrix-slot__content">
      <img :src="img" alt="matrix-slot-img" class="matrix-slot__img" />
      <div class="matrix-slot__text">
        <h2 class="matrix-slot__title">{{ title }}</h2>
        <p class="matrix-slot__description">{{ description }}</p>
      </div>
    </div>
    <div class="matrix-slot__button">
      <img
        src="/src/assets/white-lock.svg"
        alt="matrix-slot-button"
        class="matrix-slot__button-icon"
      />
    </div>
  </div>
</template>
<style lang="less" scoped>
@import "../styles/variables.less";
.matrix-slot {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
  background-color: @color-default-grey;
  gap: 16px;
  border-radius: 20px;
  padding: 12px;

  @media (max-width: @laptop) {
    gap: 14px;
    border-radius: 18px;
    padding: 10px;
  }

  @media (max-width: @tablet) {
    gap: 12px;
    border-radius: 16px;
    padding: 8px;
  }

  @media (max-width: @mobile) {
    gap: 10px;
    border-radius: 14px;
    padding: 6px 12px;
  }
  &__img {
    width: 232px;
    height: 88px;
    border-radius: 16px;
    object-fit: cover;
    flex-shrink: 0;

    @media (max-width: @laptop) {
      border-radius: 14px;
    }

    @media (max-width: @tablet) {
      width: 64px;
      height: 48px;
      border-radius: 12px;
    }

    @media (max-width: @mobile) {
      width: 73px;
      height: 48px;
      border-radius: 10px;
    }
  }

  &__content {
    display: flex;
    align-items: center;
    flex: 1;
    gap: 12px;

    @media (max-width: @tablet) {
      gap: 10px;
    }

    @media (max-width: @mobile) {
      gap: 8px;
    }
  }

  &__text {
    display: flex;
    flex-direction: column;
    justify-content: center;
    gap: 4px;
    flex: 1;
  }

  &__title {
    font-size: 18px;
    font-weight: 800;
    line-height: 24px;
    text-overflow: ellipsis;
    overflow: hidden;
    white-space: nowrap;

    @media (max-width: @laptop) {
      font-size: 16px;
      line-height: 22px;
    }

    @media (max-width: @tablet) {
      font-size: 15px;
      line-height: 20px;
    }

    @media (max-width: @mobile) {
      font-size: 14px;
      line-height: 18px;
    }
  }

  &__description {
    font-size: 14px;
    font-weight: 700;
    line-height: 20px;
    color: @color-grey-main;
    text-overflow: ellipsis;
    overflow: hidden;
    white-space: nowrap;

    @media (max-width: @laptop) {
      font-size: 13px;
      line-height: 18px;
    }

    @media (max-width: @tablet) {
      font-size: 12px;
      line-height: 16px;
    }

    @media (max-width: @mobile) {
      font-size: 11px;
      line-height: 14px;
    }
  }
  &__button {
    display: flex;
    align-items: center;
    justify-content: center;
    background: linear-gradient(
      90deg,
      rgba(255, 104, 217, 1) 0%,
      rgba(176, 112, 255, 1) 100%
    );
    border-radius: 12px;
    width: 48px;
    height: 48px;
    flex-shrink: 0;

    @media (max-width: @laptop) {
      width: 44px;
      height: 44px;
      border-radius: 10px;
    }

    @media (max-width: @tablet) {
      width: 40px;
      height: 40px;
      border-radius: 8px;
    }

    @media (max-width: @mobile) {
      width: 32px;
      height: 32px;
      border-radius: 6px;
    }
  }

  &__button-icon {
    width: 24px;
    height: 24px;

    @media (max-width: @laptop) {
      width: 22px;
      height: 22px;
    }

    @media (max-width: @tablet) {
      width: 20px;
      height: 20px;
    }

    @media (max-width: @mobile) {
      width: 16px;
      height: 16px;
    }
  }
}
</style>
