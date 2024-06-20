<script setup lang="ts">

</script>

<template>
  <div class="article-footer">
    <p class="article-footer__title">Новые статьи в Телеграме:</p>
    <p class="article-footer__link">@architecture_media</p>
    <button class="article-footer__button">Подписаться</button>
  </div>
</template>

<style scoped>
  .article-footer {
    margin: 0;
    padding: 0;
    margin-left: 100px;
    margin-right: 100px;
    margin-top: var(--padding-4);
    padding-bottom: 168px;
    padding-top: var(--padding-2);
    box-sizing: border-box;
    border-top: 4px solid var(--color-accent);
    display: flex;
    flex-direction: column;
    align-items: center;
  }

  .article-footer__title {
    margin: 0;
    padding: 0;
    color: var(--color-text-secondary);
    font-family: var(--font-main);
    font-size: var(--font-size-description);
    line-height: var(--line-height-description);
  }

  .article-footer__link {
    margin: 0;
    padding: 0;
    color: var(--color-text-primary);
    font-family: var(--font-main);
    font-size: var(--font-size-description);
    line-height: var(--line-height-description);
  }

  .article-footer__button {
    margin: 0;
    padding: 11px 36px;
    margin-top: var(--padding-2);
    background-color: var(--color-accent);
    color: #fff;
    font-family: var(--font-main);
    font-size: var(--font-size-description);
    line-height: var(--line-height-description);
    border: none;
    border-radius: 11px;
    box-shadow: 1px 4px rgba(0, 0, 0, 0.25);
  }

  .article-footer__button:hover {
    background-color: rgba(193, 20, 20, 0.6);
  }

  .article-footer__button:focus {
    background-color: var(--color-accent);
    outline: 2px solid black;
  }

  .article-footer__button:active {
    background-color: var(--color-accent);
    outline: none;
    box-shadow: inset 4px 5px rgba(0, 0, 0, 0.25);
  }

  @media (max-width: 768px) {
    .article-footer {
      margin-left: var(--padding-2);
      margin-right: var(--padding-2);
      padding-bottom: var(--padding-10);
    }

    .article-footer__title {
      font-size: var(--font-size-description-mobile);
    }

    .article-footer__link {
      font-size: var(--font-size-description-mobile);
    }

    .article-footer__button {
      padding-top: 11px;
      padding-bottom: 11px;
      font-size: var(--font-size-description-mobile);
      width: 100%;
    }
  }
  
</style>