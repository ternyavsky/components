<script setup lang="ts">
import { ref } from "vue";
import MatrixSlot from "./MatrixSlot.vue";
import AboutDropContent from "./AboutDropContent.vue";
import AboutDropHeader from "./AboutDropHeader.vue";
import PromotionBlock from "./PromotionBlock.vue";

const isContentVisible = ref(true);

const toggleContent = () => {
  isContentVisible.value = !isContentVisible.value;
};
</script>

<template>
  <div class="matrix-about">
    <h2 class="matrix-about__title">1. Общая информация</h2>
    <div class="matrix-about__drop">
      <AboutDropHeader :is-open="isContentVisible" @toggle="toggleContent" />
      <transition name="fade">
        <AboutDropContent v-if="isContentVisible" />
      </transition>
    </div>
    <MatrixSlot />
    <PromotionBlock />
  </div>
</template>

<style lang="less" scoped>
@import "../styles/variables.less";
.matrix-about {
  display: flex;
  flex-direction: column;
  max-width: 932px;

  @media (max-width: @laptop) {
    max-width: 100%;
  }

  @media (max-width: @tablet) {
    max-width: 100%;
  }

  @media (max-width: @mobile) {
    max-width: 100%;
  }

  &__title {
    font-size: 2rem;
    font-weight: 900;
    line-height: 40px;
    margin-bottom: 32px;

    @media (max-width: @laptop) {
      font-size: 1.75rem;
      line-height: 36px;
      margin-bottom: 28px;
    }

    @media (max-width: @tablet) {
      font-size: 1.5rem;
      line-height: 32px;
      margin-bottom: 24px;
    }

    @media (max-width: @mobile) {
      font-size: 1.75rem;
      line-height: 32px;
      margin-bottom: 20px;
    }
  }

  &__drop {
    border-radius: 44px;
    border: 1px solid rgba(236, 236, 236, 1);
    display: flex;
    flex-direction: column;
    gap: 16px;
    overflow: hidden;
    transition: all 0.3s ease;

    @media (max-width: @tablet) {
      border-radius: 32px;
      gap: 12px;
    }

    @media (max-width: @mobile) {
      border-radius: 24px;
      gap: 8px;
    }
  }
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.3s ease;
}

.fade-enter-from,
.fade-leave-to {
  opacity: 0;
}
</style>
