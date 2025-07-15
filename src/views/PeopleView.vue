<template>
  <div>
    <h1>People</h1>
    <div class="people-grid">
      <PersonCard v-for="person in people" :key="person.id" :person="person" />
    </div>
  </div>
</template>

<script setup lang="ts">
import PersonCard from '@/components/PersonCard.vue'
import { ref } from 'vue'

const people = ref([
  { id: 1, name: 'John Doe', email: 'john.doe@example.com' },
  { id: 2, name: 'Jane Doe', email: 'jane.doe@example.com' },
  { id: 3, name: 'Peter Jones', email: 'peter.jones@example.com' },
  { id: 4, name: 'Mary Smith', email: 'mary.smith@example.com' },
  { id: 5, name: 'David Williams', email: 'david.williams@example.com' },
  { id: 6, name: 'Sarah Brown', email: 'sarah.brown@example.com' },
  { id: 7, name: 'Michael Davis', email: 'michael.davis@example.com' },
  { id: 8, name: 'Jennifer Miller', email: 'jennifer.miller@example.com' }
])
</script>

<style scoped>
.people-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
  gap: 1rem;
}

@media (min-width: 1024px) {
  .people-grid {
    grid-template-columns: repeat(4, 1fr);
  }
}
</style>
