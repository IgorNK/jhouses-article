<script setup lang="ts">
  import { defineProps, defineEmits, ref } from "vue";
  import { onClickOutside } from "@vueuse/core";
  import CloseIcon from "./icons/CloseIcon.vue";

  interface Props {
    isOpen: Boolean,
  }

  const props = defineProps<Props>();
  const emit = defineEmits(["modal-close"]);

  const target = ref(null);
  onClickOutside(target, () => emit("modal-close"));
</script>

<template>
  <div v-if="isOpen" class="modal-mask">
    <div class="modal-wrapper">
      <div class="modal-container" ref="target">
        <div class="modal-body">
          <button @click.stop="emit('modal-close')" class="close-button"><CloseIcon class="close-icon" /></button>
          <slot name="content">Modal Contents</slot>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
  .modal-mask {
    position: fixed;
    z-index: 9998;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0, 0, 0, 0.5);
  }

  .modal-wrapper {
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;    
  }

  .close-button {
    position: absolute;
    margin: 0;
    padding: 0;
    right: -50px;
    top: -50px;
    width: 50px;
    height: 50px;
    border: none;
    background: none;
    cursor: pointer;
  }

  .close-icon {
    width: 100%;
    height: 100%;
  }

  .close-icon:hover {
    opacity: 50%;
  }

  .modal-container {
    max-width: 80%;
    max-height: 80%;
    margin: auto;
    background-color: transparent;
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    position: relative;
  }

  @media (max-width: 768px) {
    .close-button {
      right: -24px;
      top: -24px;
      width: 24px;
      height: 24px;
    }
  }
</style>