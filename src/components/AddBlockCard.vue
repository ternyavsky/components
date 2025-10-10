<script setup lang="ts">
defineProps<{
  isLock: boolean;
}>();
</script>
<template>
  <div class="add-block-card">
    <img
      :src="
        isLock
          ? '/src/assets/black-lock.svg'
          : '/src/assets/drop-content-girl.svg'
      "
      alt="add-block-card-img"
      class="add-block-card__img"
    />
    <div class="add-block-card__info">
      <h3 class="add-block-card__title">Прошлая жизнь</h3>
      <div class="add-block-card__description">
        <img
          v-if="!isLock"
          src="/src/assets/purple-lock.svg"
          alt="arrow-right"
          class="add-block-card__description-icon"
          width="24"
          height="24"
        />
        <p>Доступно в полной матрице</p>
      </div>
    </div>
  </div>
</template>
<style lang="less" scoped>
@import "../styles/variables.less";
.add-block-card {
  background-color: @color-default-grey;
  border-radius: 20px;
  padding: 16px;
  display: flex;
  flex-direction: row;
  gap: 16px;
  align-items: center;
  min-height: 80px;
  min-width: 280px;

  @media (max-width: @laptop) {
    border-radius: 18px;
    padding: 14px;
    gap: 14px;
    min-height: 72px;
    min-width: 260px;
  }

  @media (max-width: @tablet) {
    border-radius: 16px;
    padding: 12px;
    gap: 12px;
    min-height: 64px;
    min-width: 240px;
  }

  @media (max-width: @mobile) {
    border-radius: 14px;
    padding: 10px;
    gap: 10px;
    min-height: 56px;
    min-width: 220px;
  }

  &__img {
    width: 64px;
    height: 64px;
    object-fit: contain;
    border-radius: 12px;
    flex-shrink: 0;

    @media (max-width: @laptop) {
      width: 56px;
      height: 56px;
      border-radius: 10px;
    }

    @media (max-width: @tablet) {
      width: 48px;
      height: 48px;
      border-radius: 8px;
    }

    @media (max-width: @mobile) {
      width: 44px;
      height: 44px;
      border-radius: 6px;
    }
  }

  &__info {
    display: flex;
    flex-direction: column;
    justify-content: center;
    flex: 1;
    min-width: 0;

    @media (max-width: @laptop) {
      gap: 6px;
    }

    @media (max-width: @tablet) {
      gap: 4px;
    }

    @media (max-width: @mobile) {
      gap: 4px;
    }
  }

  &__title {
    font-size: 20px;
    font-weight: 800;
    line-height: 28px;
    margin: 0;
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;

    @media (max-width: @laptop) {
      font-size: 18px;
      line-height: 26px;
    }

    @media (max-width: @tablet) {
      font-size: 16px;
      line-height: 24px;
    }

    @media (max-width: @mobile) {
      font-size: 15px;
      line-height: 22px;
    }
  }

  &__description {
    display: flex;
    align-items: center;
    gap: 10px;
    font-size: 15px;
    font-weight: 700;
    line-height: 28px;
    color: @color-grey-main;
    margin: 0;
    white-space: nowrap;
    overflow: hidden;
    text-overflow: ellipsis;

    @media (max-width: @laptop) {
      font-size: 14px;
      line-height: 26px;
      gap: 8px;
    }

    @media (max-width: @tablet) {
      font-size: 13px;
      line-height: 24px;
      gap: 6px;
    }

    @media (max-width: @mobile) {
      font-size: 12px;
      line-height: 22px;
      gap: 4px;
    }
  }

  &__description-icon {
    @media (max-width: @tablet) {
      display: none;
    }
    margin-bottom: 2px;
    flex-shrink: 0;
  }
}
</style>
