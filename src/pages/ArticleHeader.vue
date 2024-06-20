<script setup lang="ts">
  import QuoteBlock from "../components/QuoteBlock.vue";
  const titleUrl = new URL('../assets/images/article_title.png', import.meta.url).href;
</script>

<template>
  <div class="article-header">
    <div class="image-block" :style="{'background-image': 'url(' + titleUrl + ')'}"/>
    <p class="image-alt">Украшение окон</p>
    <QuoteBlock class="quote-block">
      Традиционный японский дом&nbsp— это не&nbspтолько красивое и&nbspфункциональное строение, но&nbspи&nbspодин из&nbspважнейших символов японской культуры.
    </QuoteBlock>
    <div class="author-block">
      <p class="author-title">Автор статьи:</p>
      <p class="author-name">Александра Александрова</p>
    </div>
    
  </div>
  
</template>

<style scoped>
  .article-header {
    margin: 0;
    margin-right: 100px;
    margin-top: var(--padding-3);
    padding: 0;
    display: flex;
    flex-direction: row;
    column-gap: 73px;
    display: grid;
    grid-template-columns: 2fr 1fr;
    grid-template-rows: max-content 1fr min-content;
    grid-template-areas:
      "image quote"
      "image author"
      "alt none";
    max-width: 1440px;
  }

  .image-block {
    margin: 0;
    padding: 0;
    grid-area: image;
    background-position: right;
    height: 823px;
    max-width: 829px;
  }

  .image-alt {
    margin: 0;
    padding: 0;
    margin-top: var(--padding-2);
    margin-left: 100px;
    grid-area: alt;
    font-family: var(--font-main);
    font-size: var(--font-size-description);
    color: var(--color-text-secondary);
  }

  .quote-block {
    grid-area: quote;
    margin-top: var(--padding-16);
    color: var(--color-text-primary);
    font-family: var(--font-quote);
    font-size: var(--font-size-quote);
    line-height: var(--line-height-quote);
    font-weight: var(--font-weight-quote);
    font-style: italic;
  }

  .author-block {
    margin: 0;
    padding: 0;
    grid-area: author;
    display: flex;
    flex-direction: column;
    align-self: end;
    font-family: var(--font-main);
    font-size: var(--font-size-description);
  }

  .author-title {
    padding: 0;
    margin: 0;
    color: var(--color-text-primary);
  }

  .author-name {
    padding: 0;
    margin: 0;
    color: var(--color-text-secondary);
  }

  @media (max-width: 768px) {
    .article-header {
      max-width: 100vw;
      margin-right: var(--padding-2);
      margin-top: var(--padding-2);
      display: flex;
      flex-direction: column;
    }
    
    .image-block {
      background-position: right;
      max-width: calc(264/320 * 100%);
    }

    .image-alt {
      margin-top: 0;
      padding-top: var(--padding-1);
      font-size: var(--font-size-description-mobile);
      margin-left: var(--padding-2);
      font-size: var(--font-size-description-mobile);
    }

    .quote-block {
      margin-top: var(--padding-3);
      font-size: var(--font-size-quote-mobile);
      margin-left: var(--padding-2);
    }

    .author-block {
      margin-top: var(--padding-3);
      margin-left: var(--padding-2);
      align-self: start;
      font-size: var(--font-size-description-mobile);
    }
  }
  
</style>