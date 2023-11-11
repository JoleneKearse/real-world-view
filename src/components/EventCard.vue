<script setup>

defineProps({
  event: {
    type: Object,
    required: true
  },
})
</script>

<template>
  <RouterLink class="event-link" :to="{ name: 'event-details', params: { id: event.id } }">
    <div class="event-card">
      <h2>{{ event.title }}</h2>
      <span>@{{ event.time }} on {{ event.date }}</span>
    </div>
  </RouterLink> 
</template>

<style scoped>
.event-card {
  width: 250px;
  margin-bottom: 18px;
  padding: 20px;
  border: 1px solid #39495c;
  cursor: pointer;
}
.event-card:hover,
.event-card:focus {
  transform: scale(1.01);
  box-shadow: 0 3px 12px 0 rgba(0, 0, 0, 0.2);
}
.event-link {
  color: #2c3e50;
  text-decoration: none;
}
</style>
