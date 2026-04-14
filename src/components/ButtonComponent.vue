<script setup lang="ts">
defineProps<{
  href: string;
}>();
</script>
<template>
  <a class="btn" :href="href">
    <slot></slot>
  </a>
</template>
<style scoped>
.btn {
  width: 100%;
  background-color: var(--gray-700);
  color: var(--white);
  font: var(--preset-02-bold);
  text-decoration: none;
  padding: var(--spacing-150);
  border-radius: var(--spacing-100);
  display: flex;
  transition:
    background-color 0.3s ease,
    color 0.3s ease;
  justify-content: center;
}

.btn:focus,
.btn:active {
  background-color: var(--green);
  color: var(--gray-700);

  transition:
    background-color 0.3s ease,
    color 0.3s ease;
}

.btn:hover {
  background-color: var(--green);
  color: var(--gray-700);
}

.btn:focus-visible {
  outline: 3px solid var(--green);
  outline-offset: 3px;
}
</style>
