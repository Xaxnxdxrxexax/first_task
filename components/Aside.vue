<script setup>
const info = [
  {
    title: "Nyhetssak 1",
    description:
      "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque sed libero facilisis, ullamcorper ex ac, ultricies diam. In consectetur venenatis ligula at ultrices. Nunc tincidunt quam at venenatis lacinia.",
    link: "/pictures/nyhetssak.png",
  },
  {
    title: "Nyhetssak 2",
    description:
      "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque sed libero facilisis, ullamcorper ex ac, ultricies diam. In consectetur venenatis ligula at ultrices. Nunc tincidunt quam at venenatis lacinia.",
    link: "/pictures/nyhetssak.png",
  },
  {
    title: "Nyhetssak 3",
    description:
      "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Pellentesque sed libero facilisis, ullamcorper ex ac, ultricies diam. In consectetur venenatis ligula at ultrices. Nunc tincidunt quam at venenatis lacinia.",
    link: "/pictures/nyhetssak.png",
  },
];
</script>
<template>
  <div class="container">
    <hr />
    <h3>Aktuelle saker</h3>
    <div class="groupAside">
      <aside class="singleAside" v-for="item in info">
        <div><img :src="item.link" :alt="item.title" /></div>
        <div class="wrapper">
          <h4>{{ item.title }}</h4>
          <p>{{ item.description }}</p>
        </div>
      </aside>
    </div>
  </div>
</template>

<style lang="scss" scoped>
aside {
  cursor: pointer;
}
.container {
  margin-inline: 1rem;
  color: black;
  max-width: 1170px;
  margin-bottom: 3rem;
}

hr {
  border-top: 1px solid #ccc;
  box-shadow: 0px 1px 1px 0px rgba(0, 0, 0, 0.25);
  margin-bottom: 2.1rem;
}

h3 {
  font-size: clamp(1rem, 1.5rem, 2rem);
  font-weight: 400;
  margin-bottom: 2.3rem;
}

h4 {
  margin-block: 12px;
  font-size: 18px;
  font-weight: 400;
}

p {
  font-size: 15px;
  font-weight: 300;
}

.groupAside {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

@media (min-width: 768px) {
  .groupAside {
    flex-direction: row;
    gap: 1rem;
    justify-content: space-between;
  }

  .container {
    margin-inline: auto;
    margin-bottom: 83px;
  }

  aside {
    flex-basis: 320px;
  }
}
</style>
