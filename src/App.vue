<script setup lang="ts">
  import InputText from '@/InputText.vue';
  import { ref } from 'vue';
  const value = ref('');
</script>

<template>
  <InputText v-model="value" />
  <InputText :model-value="value" @update:model-value="value = $event" />
</template>
