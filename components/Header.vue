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
        :class="!isOpen ? 'burger-active' : 'burger-inactive'"
        class="burger"
        @click="isOpen = !isOpen"
      >
        <span class="sr-only">Menu</span>
      </button>
      <div :class="{ hidden: !isOpen }" class="nav-background"></div>
      <nav :class="{ 'hidden-nav': !isOpen }">
        <p><span class="lang">EN</span> | <span class="lang">NO</span></p>
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
.wrapper {
  display: flex;
  padding-inline: 19.53%;
  justify-content: space-between;
  align-items: center;
  height: 140px;
}

.header {
  background-color: #586e72;
  min-height: 140px;
  color: white;
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
  border: 0;
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

.nav-background {
  z-index: 98;
  inset: 0 0 0 0;
  background-color: rgba(0, 0, 0, 0.1);
  backdrop-filter: blur(5px);
  position: absolute;
}

.hidden {
  display: none;
}
.hidden-nav {
  display: none;
}

nav {
  position: absolute;
  inset: 0 0 0 30%;
  padding: 1rem;
  background-color: #586e72;
  z-index: 99;
  padding-inline: 19.53%;

  ul {
    display: flex;
    flex-direction: column;
    align-items: stretch;
    gap: 1rem;
    margin-top: 1rem;
    margin: 0;
    margin-top: 2rem;
    padding: 0;
  }

  li {
    list-style-type: none;
    cursor: pointer;
    text-shadow: 1px 1px 0px rgba(0, 0, 0, 0.75);
    font-family: "Roboto";
    font-size: 20px;
    font-style: normal;
    font-weight: 500;
    line-height: normal;
  }

  li:hover {
    text-decoration: underline;
  }

  li:first-of-type {
    margin-top: 1rem;
  }

  .lang {
    cursor: pointer;
    color: #fff;
    text-shadow: 1px 1px 0px rgba(0, 0, 0, 0.75);
    font-family: "Roboto";
    font-size: 18px;
    font-style: normal;
    font-weight: 400;
    line-height: normal;
  }

  .lang:hover {
    text-decoration: underline;
  }
}

@media (min-width: 768px) {
  .wrapper {
    padding-inline: 2rem;
    margin-inline: auto;
    max-width: 1500px;
  }
  .burger {
    display: none;
  }

  .nav-background {
    display: none;
  }

  .hidden-nav {
    display: flex;
  }

  nav {
    position: static;
    height: 140px;
    padding-top: 26px;
    padding-bottom: 18px;
    padding-inline: 0;
    display: flex;
    flex-direction: column;
    justify-content: space-between;

    p {
      margin-left: auto;
    }

    ul {
      flex-direction: row;
      justify-content: center;
      align-items: center;
      padding-bottom: 0;
      gap: 3rem;
    }

    li:first-of-type {
      margin-top: 0;
      padding: 0;
    }
  }
}
</style>
