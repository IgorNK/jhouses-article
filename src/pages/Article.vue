<script setup lang="ts">
  import ArticleHeader from './ArticleHeader.vue';
  import ArticleFooter from './ArticleFooter.vue';
  import ArticleMain from './ArticleMain.vue';
  import ArticleLayout from './ArticleLayout.vue';
</script>

<template>
  <div class="article">
  <ArticleLayout>
    <template #header>
      <ArticleHeader />
    </template>

    <ArticleMain />

    <template #footer>
      <ArticleFooter />
    </template>    
  </ArticleLayout>
  </div>
</template>

<style scoped>
  .article {
    background-color: var(--color-background);
  }
</style>