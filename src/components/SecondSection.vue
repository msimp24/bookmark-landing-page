<script setup>
import { ref } from 'vue'

const tabs = ref([
  {
    tab: 'Simple bookmarking',
    header: 'Bookmark in one click',
    info: 'Organize your bookmarks however you like. Our simple drag-and-drop interface gives you complete control over how you manage your favourite sites.',
    link: './../../src/assets/bookmark-landing-page-master/images/illustration-features-tab-1.svg'
  },
  {
    tab: 'Speedy Searching',
    header: 'Intelligent search',
    info: 'Our powerful search feature will help you find saved sites in no time at all. No need to trawl through all of your bookmarks.',
    link: './../../src/assets/bookmark-landing-page-master/images/illustration-features-tab-2.svg'
  },
  {
    tab: 'Easy Sharing',
    header: 'Share your bookmarks',
    info: 'Easily share your bookmarks and collections with others. Create a shareable link that you can send at the click of a button.',
    link: './../../src/assets/bookmark-landing-page-master/images/illustration-features-tab-3.svg'
  }
])
const currentTab = ref(0)
</script>

<template>
  <div class="container">
    <div class="wrapper">
      <h2>Features</h2>
      <p>
        Our aim is to make it quick and easy for you to access your favourite websites. Your
        bookmarks sync between your devices so you can access them on the go.
      </p>
    </div>
  </div>
  <div class="container">
    <div class="tabs-wrapper">
      <button
        v-for="(_, tab) in tabs"
        :key="tab"
        :class="['tab-button', { active: currentTab === tab }]"
        @click="currentTab = tab"
      >
        {{ tabs[tab].tab }}
      </button>
    </div>
  </div>
  <div class="container">
    <div class="row">
      <div class="col">
        <div class="background-img">
          <img :src="tabs[currentTab].link" alt="" />
        </div>
      </div>
      <div class="col">
        <h2>{{ tabs[currentTab].header }}</h2>
        <p>
          {{ tabs[currentTab].info }}
        </p>
        <button class="button">More Info</button>
      </div>
    </div>
  </div>
</template>

<style scoped>
.button {
  background-color: var(--soft-blue);
  border: none;
  padding: 10px 25px;
  color: white;
  border-radius: 6px;
  cursor: pointer;
  margin: 10px 0;
}
.button:hover {
  color: var(--very-dark-blue);
  background-color: white;
  outline: 2px solid var(--soft-blue);
}
.container {
  display: flex;
  justify-content: center;
}

img {
  border-radius: 20px;
}
.col + .col {
  margin-left: 60px;
}
.row {
  align-items: center;
}
.tabs-wrapper {
  width: 80%;
  height: 60px;
  display: flex;
  justify-content: center;
  align-items: center;
}
.tab-button {
  border: 0;
  background-color: white;
  padding: 20px 40px;
  color: var(--greyish-blue);
}
.tab-button:hover {
  color: var(--soft-red);
  cursor: pointer;
}
.tab-button.active {
  border-bottom: var(--soft-red) 3px solid;
  color: var(--very-dark-blue);
}

@media (width < 600px) {
  .tabs-wrapper {
    flex-direction: column;
  }
  .tab-button {
    border-bottom: var(--greyish-blue) 1px solid;
    width: 70%;
  }
  .row {
    flex-direction: column;
    margin: 30px 0;
  }
  .col {
    text-align: center;
  }
}
</style>
