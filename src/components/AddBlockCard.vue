<script setup lang="ts"></script>
<template>
  <div class="add-block-card">
    <img
      src="/src/assets/drop-content-girl.svg"
      alt="add-block-card-img"
      class="add-block-card__img"
    />
    <div class="add-block-card__info">
      <h3 class="add-block-card__title">Прошлая жизнь</h3>
      <div class="add-block-card__description">
        <img
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

  @media (max-width: @laptop) {
    border-radius: 18px;
    padding: 14px;
    gap: 14px;
    min-height: 72px;
  }

  @media (max-width: @tablet) {
    border-radius: 16px;
    padding: 12px;
    gap: 12px;
    min-height: 64px;
  }

  @media (max-width: @mobile) {
    border-radius: 14px;
    padding: 10px;
    gap: 10px;
    min-height: 56px;
  }

  &__img {
    width: 64px;
    height: 64px;
    object-fit: contain;
    border-radius: 12px;

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
      width: 40px;
      height: 40px;
      border-radius: 6px;
    }
  }

  &__info {
    display: flex;
    flex-direction: column;
    justify-content: center;
    gap: 8px;
    flex: 1;

    @media (max-width: @laptop) {
      gap: 6px;
    }

    @media (max-width: @tablet) {
      gap: 4px;
    }

    @media (max-width: @mobile) {
      gap: 2px;
    }
  }

  &__title {
    font-size: 1.25rem;
    font-weight: 800;
    line-height: 28px;
    margin: 0;

    @media (max-width: @laptop) {
      font-size: 1.125rem;
      line-height: 26px;
    }

    @media (max-width: @tablet) {
      font-size: 1rem;
      line-height: 24px;
    }

    @media (max-width: @mobile) {
      font-size: 0.9rem;
      line-height: 22px;
    }
  }

  &__description {
    display: flex;
    align-items: center;
    gap: 10px;
    font-size: 0.9375rem;
    font-weight: 700;
    line-height: 28px;
    color: @color-grey-main;
    margin: 0;

    @media (max-width: @laptop) {
      font-size: 0.875rem;
      line-height: 26px;
      gap: 8px;
    }

    @media (max-width: @tablet) {
      font-size: 0.8rem;
      line-height: 24px;
      gap: 6px;
    }

    @media (max-width: @mobile) {
      font-size: 0.75rem;
      line-height: 22px;
      gap: 4px;
    }
  }

  &__description-icon {
    @media (max-width: @tablet) {
      display: none;
    }
    margin-bottom: 2px;
  }
}
</style>
