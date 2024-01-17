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
      <button :class="{ hidden: isOpen }">
        <span class="sr-only">Menu</span>
      </button>
      <nav class="rightHeader">
        <p>EN | NO</p>
        <ul class="nav">
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
const isOpen = ref(true);
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

.rightHeader {
  display: flex;
  flex-direction: column;
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

.nav {
  display: flex;
  gap: 61px;
  list-style: none;
  color: #fff;
  text-shadow: 1px 1px 0px rgba(0, 0, 0, 0.75);
  font-family: "Roboto";
  font-size: 20px;
  font-style: normal;
  font-weight: 500;
  line-height: normal;
}

.hidden {
  display: none;
}

@media (max-width: 375px) {
  .rightHeader {
    display: none;
  }
}
</style>
