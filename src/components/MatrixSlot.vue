<template>
  <div class="matrix-slot">
    <div class="matrix-slot__content">
      <img
        src="/src/assets/mirror-girl.svg"
        alt="matrix-slot-img"
        class="matrix-slot__img"
      />
      <div class="matrix-slot__text">
        <h2 class="matrix-slot__title">Проработка души</h2>
        <p class="matrix-slot__description">В нынешнем воплощении</p>
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
  gap: 28px;
  border-radius: 32px;
  padding: 16px;
  @media (max-width: @mobile) {
    gap: 12px;
    border-radius: 20px;
    padding: 8px 16px;
  }
  &__img {
    max-width: 232px;
    max-height: 88px;
    width: 100%;
    height: 100%;
    border-radius: 20px;
    object-fit: contain;
    @media (max-width: @mobile) {
      max-width: 73px;
      height: 48px;
      border-radius: 12px;
      object-fit: cover;
    }
  }
  &__content {
    display: flex;
    align-items: center;
    width: 100%;
    gap: 16px;
  }
  &__text {
    display: flex;
    flex-direction: column;
    align-items: center;
  }
  &__title {
    font-size: 1.75rem;
    font-weight: 900;
    line-height: 44px;
    @media (max-width: @mobile) {
      font-size: 1.125rem;
      line-height: 24px;
      font-weight: 900;
    }
  }
  &__description {
    font-size: 1.25rem;
    font-weight: 600;
    line-height: 28px;
    @media (max-width: @mobile) {
      font-size: 0.875rem;
      line-height: 16px;
      font-weight: 600;
    }
  }
  &__button {
    display: flex;
    margin: auto;
    background: linear-gradient(
      90deg,
      rgba(255, 104, 217, 1) 0%,
      rgba(176, 112, 255, 1) 100%
    );
    border-radius: 14px;
    width: 48px;
    padding: 12px;
    height: 48px;
    @media (max-width: @mobile) {
      width: 24px;
      height: 24px;
      border-radius: 24px;
      padding: 4px;
    }
  }
}
</style>
