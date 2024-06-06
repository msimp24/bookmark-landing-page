<script setup>
import { RouterLink } from 'vue-router'
</script>

<template>
  <div class="container">
    <nav class="nav">
      <RouterLink class="logo" to="/">
        <img src="/public/images/logo-bookmark.svg" alt="" />
      </RouterLink>

      <ul class="nav-list">
        <a class="nav-link" href="">
          <li class="nav-item">FEATURES</li>
        </a>
        <a class="nav-link" href="">
          <li class="nav-item">PRICING</li>
        </a>
        <a class="nav-link" href="">
          <li class="nav-item">CONTACT</li>
        </a>
        <button>LOGIN</button>
      </ul>
    </nav>
  </div>
</template>

<style scoped>
.nav {
  width: 100%;
  height: 80px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  font-size: 14px;
}
.nav-list {
  display: flex;
  align-items: center;
}
.nav-link {
  text-decoration: none;
  list-style: none;
  color: var(--very-dark-blue);
}
.nav-item {
  margin-right: 30px;
}
button {
  background-color: var(--soft-red);
  border: none;
  padding: 10px 25px;
  color: white;
  border-radius: 6px;
  cursor: pointer;
}
button:hover {
  background-color: white;
  color: var(--soft-red);
  outline: 2px solid var(--soft-red);
}
.nav-item:hover {
  color: var(--soft-red);
}

@media (width < 700px) {
}
</style>
