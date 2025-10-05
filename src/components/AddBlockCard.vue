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
  padding: 12px;
  display: flex;
  flex-direction: row;
  gap: 12px;
  align-items: center;

  &__img {
    width: 64px;
    height: 64px;
    object-fit: contain;
    border-radius: 12px;
  }
  &__info {
    display: flex;
    flex-direction: column;

    gap: 4px;
    @media (max-width: @mobile) {
      gap: 0px;
    }
    &__title {
      font-size: 1.25rem;
      font-weight: 800;
      line-height: 28px;
    }
    &__description {
      display: flex;
      gap: 10px;
      font-size: 0.9375rem;
      font-weight: 700;
      line-height: 28px;
      color: @color-grey-main;
    }
  }
  &__description-icon {
    @media (max-width: @mobile) {
      display: none;
    }
  }
}
</style>
