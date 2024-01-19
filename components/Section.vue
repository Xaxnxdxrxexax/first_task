<template>
  <div class="container">
    <section class="section">
      <img src="/pictures/kurs.png" alt="kurs" />
      <div class="wrapper">
        <h2 class="">Kurs og sertifisering</h2>
        <p>
          Vi har en rekke kurs og sertifiseringer,
          <span>se full liste her</span>
        </p>
        <p>Eller bruk søkefeltet under</p>
        <input type="text" placeholder="Søk i kurs og sertifisering" />
      </div>
    </section>
  </div>
</template>

<script setup></script>

<style lang="scss" scoped>
img {
  object-fit: cover;
  min-height: 320px;
}
.container {
  margin-top: 2.68rem;
  margin-inline: 1rem;
  margin-bottom: 1rem;
  max-width: 1170px;
}
.section {
  position: relative;
  width: 100%;
  max-width: 1170px;
  &::before {
    content: "";
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: linear-gradient(transparent, rgba(0, 0, 0, 0.7) 90%);
  }
}
.wrapper {
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
  padding-top: 2.6rem;
  padding-inline: 1rem;
  padding-bottom: 1.5rem;
  color: $color-secondary;
  text-shadow: 1px 1px 0px rgba(0, 0, 0, 0.75);
}
h2 {
  font-size: clamp(1rem, 1.5vw, 2.25rem);
  font-weight: 500;
  margin-bottom: 18px;
}

p {
  font-size: clamp(0.8rem, 1rem, 1.12rem);
  font-weight: 400;
  &:first-of-type {
    margin-bottom: 10px;
  }
  &:last-of-type {
    margin-bottom: 49px;
  }
}

span {
  font-size: clamp(0.8rem, 1rem, 1.12rem);
  font-weight: 700;
}

input {
  width: 100%;
  background-image: url("/icons/icon-search.svg");
  background-repeat: no-repeat;
  background-position: 99% 50%;
  background-size: 34px 30px;
  padding: 1rem;

  &::placeholder {
    color: black;
    font-size: 18px;
    font-weight: 200;
    text-align: center;
  }
}

@media (min-width: 768px) {
  .wrapper {
    padding-inline: 7.8rem;
    padding-bottom: 3.3rem;
  }

  .container {
    margin-inline: auto;
  }
}
</style>
