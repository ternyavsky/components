<script setup lang="ts"></script>
<template>
  <div class="state-block">
    <h2 class="state-block__title">Состояние человека «в плюсе»:</h2>
    <ul class="state-block__list">
      <li class="state-block__item">
        <div class="state-block__item-content">
          <span class="state-block__item-title">Проницательность.</span>
          <span class="state-block__item-description">
            Такой человек очень проницателен, быстро понимает истинные причины
            происходящего, хорошо чувствует мотивы и предвидит события. Хочет
            разобраться в мельчайших подробностях, всегда и всё любит
            «раскладывать по полочкам», и это обычно ему удаётся.
          </span>
        </div>
      </li>
      <li class="state-block__item">
        <div class="state-block__item-content">
          <span class="state-block__item-title">Баланс.</span>
          <span class="state-block__item-description">
            Стремится соблюдать баланс во всём. Работать и заниматься спортом,
            питаться вкусно, но невредно, строить карьеру и не забывать о семье
            и т. д. Задача это сложная, но 8 аркан не опускает рук и терпеливо
            строит систему сдержек и противовесов.
          </span>
        </div>
      </li>
      <li class="state-block__item">
        <div class="state-block__item-content">
          <span class="state-block__item-title">Закон и совесть.</span>
          <span class="state-block__item-description">
            Это прямой, открытый человек, беспристрастный. Всегда держит слово,
            соблюдает юридические и моральные законы, очень переживает, если
            приходится идти против совести. Очень теряется, когда не может
            ничего сделать законными методами. 
          </span>
        </div>
      </li>
      <li class="state-block__item">
        <div class="state-block__item-content">
          <span class="state-block__item-title">Здравый смысл.</span>
          <span class="state-block__item-description">
            Этот человек умеет справляться с эмоциями, здраво смотреть на всё
            происходящее, руководствуясь логикой. Редко нервничает, умеет
            сосредоточиться на деле, независим от мнения окружающих.
          </span>
        </div>
      </li>
      <li class="state-block__item">
        <div class="state-block__item-content">
          <span class="state-block__item-title">Поиск правильного пути.</span>
          <span class="state-block__item-description">
            Всегда старается найти правильное решение, иногда пренебрегая более
            выгодными и заманчивыми вариантами. За это окружающие считают его
            наивным идеалистом.
          </span>
        </div>
      </li>
    </ul>
  </div>
</template>
<style lang="less" scoped>
@import "../styles/variables.less";
.state-block {
  background: @color-default-grey;
  border-radius: 32px;
  padding: 40px 32px;

  @media (max-width: @laptop) {
    padding: 32px 24px;
    border-radius: 28px;
  }

  @media (max-width: @tablet) {
    padding: 24px 20px;
    border-radius: 24px;
  }

  @media (max-width: @mobile) {
    padding: 20px 16px;
    border-radius: 20px;
  }

  &__title {
    font-size: 1.25rem;
    font-weight: 800;
    line-height: 28px;
    margin-bottom: 16px;

    @media (max-width: @laptop) {
      font-size: 1.5rem;
      line-height: 26px;
      margin-bottom: 14px;
    }

    @media (max-width: @tablet) {
      font-size: 1.4rem;
      line-height: 24px;
      margin-bottom: 12px;
    }

    @media (max-width: @mobile) {
      font-size: 1.3em;
      line-height: 22px;
      margin-bottom: 10px;
    }
  }

  &__list {
    list-style: none;
    padding: 0;
    margin: 0;
    display: flex;
    flex-direction: column;
    gap: 20px;

    @media (max-width: @laptop) {
      gap: 18px;
    }

    @media (max-width: @tablet) {
      gap: 16px;
    }

    @media (max-width: @mobile) {
      gap: 14px;
    }
  }

  &__item {
    position: relative;
    padding-left: 20px;

    @media (max-width: @tablet) {
      padding-left: 18px;
    }

    @media (max-width: @mobile) {
      padding-left: 16px;
    }

    &::before {
      content: "";
      width: 4px;
      height: 4px;
      background-color: @color-text-red;
      border-radius: 50%;
      position: absolute;
      left: 0;
      top: 10px;

      @media (max-width: @tablet) {
        width: 3px;
        height: 3px;
        top: 8px;
      }

      @media (max-width: @mobile) {
        width: 3px;
        height: 3px;
        top: 6px;
      }
    }
  }

  &__item-title {
    font-weight: 800;
    color: @color-text-red;
    font-size: 1.0625rem;
    line-height: 28px;

    @media (max-width: @laptop) {
      font-size: 1rem;
      line-height: 26px;
    }

    @media (max-width: @tablet) {
      font-size: 0.9rem;
      line-height: 24px;
    }

    @media (max-width: @mobile) {
      font-size: 0.875rem;
      line-height: 22px;
      font-weight: 600;
    }
  }

  &__item-description {
    font-size: 1.0625rem;
    font-weight: 600;
    line-height: 28px;
    color: @color-black-main;

    @media (max-width: @laptop) {
      font-size: 1rem;
      line-height: 26px;
    }

    @media (max-width: @tablet) {
      font-size: 0.9rem;
      line-height: 24px;
    }

    @media (max-width: @mobile) {
      font-size: 0.875rem;
      line-height: 22px;
      font-weight: 600;
    }
  }
}
</style>
