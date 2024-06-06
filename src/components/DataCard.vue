<script setup>
defineProps(['data'])
</script>

<template>
  <div v-if="data" class="card">
    <img class="logo" :src="data.link" alt="" />
    <h4>{{ data.header }}</h4>
    <p>{{ data.version }}</p>
    <img class="dots" src="./../assets/bookmark-landing-page-master/images/bg-dots.svg" alt="" />
    <button>Add & Install Extension</button>
  </div>
</template>

<style scoped>
.dots {
  margin-top: 14px;
}
.card {
  display: flex;
  flex-direction: column;
  align-items: center;
  max-width: 300px;
  box-shadow:
    rgba(0, 0, 0, 0.1) 0px 10px 15px -3px,
    rgba(0, 0, 0, 0.05) 0px 4px 6px -2px;
  padding: 20px;
  gap: 10px;
  border-radius: 10px;
  margin: 0 15px;
}

button {
  padding: 14px 16px;
  border: none;
  border-radius: 6px;
  font-size: 12px;
  box-shadow:
    rgba(0, 0, 0, 0.1) 0px 10px 15px -3px,
    rgba(0, 0, 0, 0.05) 0px 4px 6px -2px;
  cursor: pointer;
  margin: 10px 0;
  background-color: var(--soft-blue);
  color: white;
  cursor: pointer;
}

button:hover {
  outline: 2px solid var(--soft-blue);
  background-color: white;
  color: var(--very-dark-blue);
}

.logo {
  height: 60px;
  width: 60px;
}
</style>
