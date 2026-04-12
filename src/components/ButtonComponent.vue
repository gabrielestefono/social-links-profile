<script setup lang="ts"></script>
<template>
  <a class="btn" href="#">
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

.btn:hover,
.btn:focus,
.btn:active,
.btn:focus-visible {
  background-color: var(--green);
  color: var(--gray-700);

  transition:
    background-color 0.3s ease,
    color 0.3s ease;
}
</style>
