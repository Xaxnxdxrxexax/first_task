<template>
  <header class="header">
    <div class="wrapper">
      <div>
        <img
          src="../assets/logo/GroupglassPaperLogo.png"
          alt="glassPaper logo"
          class="logo"
        />
      </div>
      <button
        :class="isOpen ? 'burger-active' : 'burger-inactive'"
        class="burger"
        @click="isOpen = !isOpen"
      >
        <span class="sr-only">Menu</span>
      </button>
      <nav v-if="isOpen" class="nav-background"></nav>
      <nav v-if="isOpen" class="rightHeader">
        <p class="lang">EN | NO</p>
        <ul class="nav-list">
          <li>Tjenester</li>
          <li>Om oss</li>
          <li>Kontakt oss</li>
          <li>Ledige stillinger</li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<script setup>
const isOpen = ref(false);
</script>

<style scoped>
.header {
  background-color: #586e72;
  min-height: 140px;
  color: white;
}
.wrapper {
  display: flex;
  padding-inline: 19.53%;
  justify-content: space-between;
  align-items: center;
  height: 140px;
}

.hidden {
  display: none;
}

.nav-background {
  z-index: 98;
  inset: 0 0 0 0;
  background-color: rgba(0, 0, 0, 0.2);
  filter: blur(4px);
}

.burger {
  display: block;
  position: absolute;
  right: 1rem;
  top: 1rem;
  background: transparent;
  background-repeat: no-repeat;
  background-position: center;
  z-index: 100;
}

.burger-active {
  background-image: url(~/assets/icon-hamburger.svg);
  width: 24px;
  height: 21px;
}

.burger-inactive {
  background-image: url(~/assets/icon-close.svg);
  width: 20px;
  height: 21px;
}

.nav-list {
  position: fixed;
  inset: 0 0 0 30%;
  list-style: none;
  margin: 0;
  display: flex;
  flex-direction: column;
  padding: 2rem;
  z-index: 99;
  background-color: #586e72;

  li {
    list-style-type: none;
    margin-bottom: 1rem;
    cursor: pointer;
  }

  li:first-of-type {
    margin-top: 1rem;
  }

  li:hover {
    text-decoration: underline;
  }
}
.lang {
  cursor: pointer;
}
.lang:hover {
  text-decoration: underline;
}
@media (min-width: 376px) {
  .nav-background {
    display: none;
  }
  .nav {
    position: static;
    inset: none;
    outline: 1px solid black;
    display: flex;
    flex-direction: row;
    gap: 61px;
    list-style: none;
    color: #fff;
    text-shadow: 1px 1px 0px rgba(0, 0, 0, 0.75);
    font-family: "Roboto";
    font-size: 20px;
    font-style: normal;
    font-weight: 500;
    line-height: normal;
    align-self: stretch;
    justify-content: space-between;

    p {
      margin-left: auto;
      color: #fff;
      text-shadow: 1px 1px 0px rgba(0, 0, 0, 0.75);
      font-family: "Roboto";
      font-size: 18px;
      font-style: normal;
      font-weight: 400;
      line-height: normal;
    }
  }
}
</style>
