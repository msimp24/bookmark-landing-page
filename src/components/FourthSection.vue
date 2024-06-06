<script setup>
import { ref } from 'vue'

const faqs = ref([
  {
    question: 'What is Bookmark',
    content:
      'Lorem ipsum dolor sit amet consectetur, adipisicing elit. Recusandae numquam est voluptatibus iste nisi. Doloribus vel explicabo nesciunt, recusandae reprehenderit iure nihil labore natus dicta debitis. Iusto dignissimos mollitia deleniti!',
    clicked: false
  },
  {
    question: 'How can I request a new browser?',
    content:
      'Lorem ipsum dolor sit amet consectetur, adipisicing elit. Recusandae numquam est voluptatibus iste nisi. Doloribus vel explicabo nesciunt, recusandae reprehenderit iure nihil labore natus dicta debitis. Iusto dignissimos mollitia deleniti!',
    clicked: false
  },
  {
    question: 'Is there a mobile app?',
    content:
      'Lorem ipsum dolor sit amet consectetur, adipisicing elit. Recusandae numquam est voluptatibus iste nisi. Doloribus vel explicabo nesciunt, recusandae reprehenderit iure nihil labore natus dicta debitis. Iusto dignissimos mollitia deleniti!',
    clicked: false
  },
  {
    question: 'What about the chromium browsers',
    content:
      'Lorem ipsum dolor sit amet consectetur, adipisicing elit. Recusandae numquam est voluptatibus iste nisi. Doloribus vel explicabo nesciunt, recusandae reprehenderit iure nihil labore natus dicta debitis. Iusto dignissimos mollitia deleniti!',
    clicked: false
  }
])
</script>

<template>
  <div class="wrapper">
    <h2>Frequently asked questions</h2>
    <p>
      Here are some of our FAQs. If you have any other questions you'd like answered, please feel
      free to reach out to us.
    </p>
    <div class="col">
      <div v-for="(item, index) in faqs" :key="index" class="accordion">
        <div @click="item.clicked = !item.clicked" class="accordion-item">
          <div class="accordion-container">
            <h2 class="accordion-title" :class="{ active: item.clicked }">
              {{ item.question }}
            </h2>
            <img
              src="./../assets/bookmark-landing-page-master/images/icon-arrow.svg"
              alt=""
              class="icon"
              :class="{ active: item.clicked }"
            />
          </div>

          <div :class="{ active: item.clicked }" class="accordion-content">
            <p>{{ item.content }}</p>
          </div>
        </div>
      </div>
      <button class="button">More Info</button>
    </div>
  </div>
</template>

<style scoped>
button {
  background-color: var(--soft-blue);
  border: none;
  padding: 10px 25px;
  color: white;
  border-radius: 6px;
  cursor: pointer;
  margin: 40px 0;
}
button:hover {
  color: var(--very-dark-blue);
  background-color: white;
  outline: solid 2px var(--soft-blue);
}
.accordion {
  border-top: 1px solid var(--very-dark-blue);
  margin: 10px 0;
}
.accordion-content {
  max-height: 0;
  overflow: hidden;
  transition: max-height 0.3s ease;
}
.accordion-title {
  font-size: 16px;
}
.accordion-title.active {
  color: var(--soft-red);
}
.accordion-title:hover {
  color: var(--soft-red);
}
.accordion-container {
  cursor: pointer;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.accordion-content.active {
  max-height: 120px; /* Adjust height as needed */
}
.icon.active {
  transform: rotate(180deg);
}
.col {
  margin-top: 20px;
}
.accordion: nth-child(2);
</style>
