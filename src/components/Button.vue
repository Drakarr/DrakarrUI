<template>
  <button class="btn" :class="classBinding">
    <slot />
  </button>
</template>

<script setup lang="ts">
import { computed } from 'vue';
import '@/assets/tailwind.scss';

const props = defineProps<{ btnPrimary?: boolean }>();

const classBinding = computed(() => ({
  'btn-primary': !!props.btnPrimary,
}));
</script>
