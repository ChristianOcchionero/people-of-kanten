<template>
  <div class="person-card">
    <h3>{{ person.name }}</h3>
    <p>{{ person.email }}</p>
  </div>
</template>

<script setup lang="ts">
defineProps<{
  person: {
    name: string
    email: string
  }
}>()
</script>

<style scoped>
.person-card {
  border: 1px solid #ccc;
  padding: 1rem;
  margin: 1rem;
  border-radius: 5px;
}
</style>
