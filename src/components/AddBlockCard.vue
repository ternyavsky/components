<script setup lang="ts"></script>
<template>
  <div class="add-block-card">
    <img
      src="/src/assets/drop-content-girl.svg"
      alt="add-block-card-img"
      class="add-block-card__img"
    />
    <div class="add-block-card__info">
      <h3 class="add-block-card__info__title">Прошлая жизнь</h3>
      <div class="add-block-card__info__description">
        <img
          src="/src/assets/purple-lock.svg"
          alt="arrow-right"
          class="add-block-card__info__description__icon"
          width="24"
          height="24"
        />
        <p>Доступно в полной матрице</p>
      </div>
    </div>
  </div>
</template>
<style lang="less" scoped>
.add-block-card {
  background-color: var(--color-default-grey);
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
      font-size: 20px;
      font-weight: 800;
      line-height: 28px;
    }
    &__description {
      display: flex;
      gap: 10px;
      font-size: 15px;
      font-weight: 700;
      line-height: 28px;
      color: var(--color-grey-main);
      &__icon {
        @media (max-width: @mobile) {
          display: none;
        }
      }
    }
  }
}
</style>
