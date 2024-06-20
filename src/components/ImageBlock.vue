<script setup lang="ts">
  import { ref, toRefs } from "vue";

  interface Props {
    src: string;
    alt: string;
  }

  const props = defineProps<Props>();
  const { src, alt } = toRefs(props);

  const emit = defineEmits(['click']);
  const handleClick = (event) => {
    emit('click', props.src);
  };
  
</script>

<template>
  <div @click="handleClick" class="image-container">
    <img :src="src" :alt="alt" />
    <p class="text">{{ alt }}</p>
  </div>
  
</template>

<style scoped>
  .image-container {
    margin: 0;
    padding: 0;
    display: flex;
    flex-direction: column;
    row-gap: var(--padding-2);    
  }

  .image-container:hover {
    opacity: 50%;
    cursor: pointer;
  }

  .text {
    margin: 0;
    padding: 0;
    color: var(--color-text-secondary);
    font-family: var(--font-main);
    font-size: var(--font-size-description);
    line-height: var(--line-height-description);
  }

  @media (max-width: 768px) {
    .image-container {
      row-gap: var(--padding-1);      
    }

    .text {
      font-size: var(--font-size-description-mobile);
      font-size: var(--font-size-description-mobile);
    }
  }
</style>