<script setup></script>

<template>
  <div class="container">
    <div class="row">
      <div class="col">
        <h1>A Simple Bookmark Manager</h1>
        <p>
          A clean and simple interface to organize your favorite websites. Open a new browser tab
          and see your sites load instantly. Try it for free.
        </p>
        <div>
          <button class="chrome">Get it on Chrome</button>
          <button class="firefox">Get in on Firefox</button>
        </div>
      </div>
      <div class="col">
        <div class="background-img">
          <img src="../assets/bookmark-landing-page-master/images/illustration-hero.svg" alt="" />
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
h1 {
  color: var(--very-dark-blue);
}
p {
  color: var(--very-dark-blue);
  font-weight: 300;
  margin: 1rem 0;
  line-height: 20px;
}

.col + .col {
  margin-left: 60px;
}
.row {
  align-items: center;
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
}
button:hover {
  background-color: white;
}
.chrome:hover {
  outline: 2px solid var(--soft-blue);
  color: var(--soft-blue);
}
.chrome {
  margin-right: 10px;
  background-color: var(--soft-blue);
  color: white;
}
.firefox {
  color: var(--very-dark-blue);
}
.firefox:hover {
  outline: var(--very-dark-blue) solid 2px;
}
img {
  border-radius: 20px;
  position: relative;
  bottom: 70px;
  right: 50px;
}
.background-img {
  background-color: var(--soft-blue);
  width: 100%;
  border-radius: 50% 0px 0px 50%;
}
.container {
  margin-top: 2rem;
}

@media (width < 600px) {
  .row {
    flex-direction: column-reverse;
  }
  .col {
    margin-top: 30px;
    text-align: center;
  }
}
</style>
