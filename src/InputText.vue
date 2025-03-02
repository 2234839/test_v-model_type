<style scoped></style>
<template>
  <input type="text" v-model="modelValue" />
</template>
<script setup lang="ts">
  const modelValue = defineModel<string | undefined>();
</script>
