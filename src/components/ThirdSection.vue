<script setup>
import DataCard from '@/components/DataCard.vue'

import { ref } from 'vue'

const cardData = ref([
  {
    link: '/logo-chrome.svg',
    header: 'Add to Chrome',
    version: 'Minimum version 62'
  },
  {
    link: '/logo-firefox.svg',
    header: 'Add to Firefox',
    version: 'Minimum version 55'
  },
  {
    link: '/logo-opera.svg',
    header: 'Add to Opera',
    version: 'Minimum version 46'
  }
])
</script>

<template>
  <div class="wrapper">
    <h2>Download the extension</h2>
    <p>
      We've got more browsers in the pipeline. Please do let us know if you've got a favourite you
      would like to prioritize.
    </p>
  </div>

  <div class="container">
    <div class="row">
      <div v-for="data in cardData" :key="data" class="col">
        <DataCard :data="data" />
      </div>
    </div>
  </div>
</template>

<style scoped>
.row {
  display: flex;
}
.col:nth-child(2) {
  margin-top: 60px;
}
.col:nth-child(3) {
  margin-top: 120px;
}

@media (width < 600px) {
  .col {
    margin: 20px 0;
  }
  .row {
    flex-direction: column;
  }
  .container {
    display: flex;
    justify-content: center;
  }
  .col:nth-child(2) {
    margin-top: 0px;
  }
  .col:nth-child(3) {
    margin-top: 0px;
  }
}
</style>
