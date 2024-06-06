<script setup></script>

<template>
  <div class="footer">
    <div class="wrapper">
      <p>35,000+ ALREADY JOINED</p>
      <h2>Stay up-to-date with what we're doing</h2>
      <div class="input-container">
        <input class="email-input" type="text" />
        <button>Contact Us</button>
      </div>
    </div>
  </div>
  <div class="bottom-footer">
    <div class="container">
      <nav class="nav">
        <ul class="nav-list">
          <div class="link-container">
            <a class="nav-link" href="">
              <li class="nav-item">FEATURES</li>
            </a>
            <a class="nav-link" href="">
              <li class="nav-item">PRICING</li>
            </a>
            <a class="nav-link" href="">
              <li class="nav-item">CONTACT</li>
            </a>
          </div>

          <div class="icons-container">
            <img
              class="icon"
              src="./../assets/bookmark-landing-page-master/images/icon-facebook.svg"
              alt=""
            />
            <img
              class="icon"
              src="./../assets/bookmark-landing-page-master/images/icon-twitter.svg"
              alt=""
            />
          </div>
        </ul>
      </nav>
    </div>
  </div>
</template>

<style scoped>
.nav {
  display: flex;
}
.nav-list {
  display: flex;
  align-items: center;
  width: 100%;
  justify-content: space-between;
}
.link-container {
  display: flex;
  justify-content: space-between;
  width: 40%;
  max-width: 350px;
  gap: 20px;
}
.nav-link {
  text-decoration: none;
  list-style-type: none;
  color: white;
  margin-top: 10px;
}
.nav-item {
  font-size: 14px;
  letter-spacing: 2px;
}
.nav-item:hover {
  color: var(--soft-red);
}
.icons-container {
  display: flex;
  gap: 14px;
}
.icon:hover {
  color: var(--soft-red);
  cursor: pointer;
}
.footer {
  width: 100%;
  background-color: var(--soft-blue);
}
.bottom-footer {
  width: 100%;
  background-color: var(--very-dark-blue);
}
.wrapper {
  padding: 40px 0;
}
p {
  color: white;
  font-size: 10px;
  font-weight: 400;
  letter-spacing: 4px;
}
h2 {
  color: white;
}
button {
  background-color: var(--soft-red);
  border: none;
  height: 100%;
  padding: 0 20px;
  color: white;
  border-radius: 2px;
  cursor: pointer;
}
button:hover {
  color: var(--very-dark-blue);
  background-color: white;
  outline: solid 2px var(--soft-red);
}
.email-input {
  height: 100%;
  width: 100%;
  max-width: 350px;
  padding: 4px;
  margin-right: 10px;
}
.input-container {
  display: flex;
  justify-content: center;
  height: 40px;
  width: 100%;
}

@media (width < 600px) {
  .nav {
    align-items: center;
  }
  .nav-list {
    flex-direction: column;
    justify-content: center;
    text-align: center;
  }
  .link-container {
    flex-direction: column;
    justify-content: center;
    gap: 10px;
  }
  .icons-container {
    flex-direction: column;
    margin: 20px 0;
  }
}
</style>
