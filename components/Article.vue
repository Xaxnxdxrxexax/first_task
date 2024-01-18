<script setup>
const info = [
  {
    title: "Bemanning og rekruttering",
    description: "Vi finner og kurser riktige kandidater for deg",
    link: "/_nuxt/assets/pictures/bemannig.png",
  },
  {
    title: "Konsulenttjenester",
    description: "Enkeltkonsulenter eller hele prosjekter",
    link: "/_nuxt/assets/pictures/konsulenttjenester.png",
  },
  {
    title: "Programvare",
    description: "Progamvare for nanolearning og compliance",
    link: "/_nuxt/assets/pictures/compliance.png",
  },
];
</script>
<template>
  <div class="container">
    <article class="singleArticle" v-for="item in info">
      <div><img :src="item.link" :alt="item.title" /></div>
      <div class="wrapper">
        <h2>{{ item.title }}</h2>
        <p>{{ item.description }}</p>
      </div>
    </article>
  </div>
</template>

<style lang="scss" scoped>
.container {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  margin-top: 2rem;
  margin-inline: 1rem;
  margin-bottom: 2rem;
}
img {
  min-height: 320px;
  object-fit: cover;
}

article {
  position: relative;
  width: 100%;
  cursor: pointer;
}
article::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: linear-gradient(transparent, rgba(0, 0, 0, 0.7) 90%);
}

.wrapper {
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
  text-shadow: 1px 1px 0px rgba(0, 0, 0, 0.75);
  font-family: Roboto;
  color: #fff;
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
  justify-content: center;
  padding-top: 12rem;
  padding-left: 1rem;
}

h2 {
  font-size: 1.5rem;
  font-weight: 500;
}

p {
  font-size: clamp(0.8rem, 1rem, 1.12rem);
  font-weight: 400;
}

@media (min-width: 768px) {
  .container {
    flex-direction: row;
    max-width: 1170px;
    margin-inline: auto;
    gap: 2.18rem;
    margin-bottom: 5.1875rem;
  }

  article {
    flex-grow: 1;
    flex-basis: 320px;
  }

  article:first-of-type {
    flex-basis: 460px;
    flex-grow: 1.4375;
  }
}
</style>
