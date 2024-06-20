<script setup lang="ts"> 

</script>

<template>
  <blockquote class="quote">
    <slot class="inner" />
  </blockquote>
</template>

<style scoped>
  .quote {
    padding: 0 32px;
    margin: 0;    
    border-left: 4px solid var(--color-accent);
    box-sizing: border-box;    
  }

  .inner {
    margin: 0;
    padding: 0;    
  }

  @media (max-width: 768px) {
    .quote {
      padding: 0 16px;      
    }
  }
</style>