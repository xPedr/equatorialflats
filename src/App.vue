<template>
  <Nav />
  <div id="view">
    <router-view />
  </div>
  <Footer />
</template>

<script>
import Nav from "./components/Nav.vue";
import Footer from "./components/Footer.vue";

export default {
  components: {
    Nav,
    Footer,
  },
};
</script>

<style>
#app {
  font-family: sans-serif;
}

#view {
  height: 100%;
}

h1 {
  font-family: "Zen Tokyo Zoo", cursive;
  font-size: 46px;
  font-weight: 600;
  color: #4e001a;
}

h2,
h3 {
  font-family: "Bebas Neue", cursive;
  font-weight: 800;
  color: #4e001a;
  letter-spacing: 0.15em;
}

p,
h4 {
  font-family: "PT Sans", sans-serif;
  color: black;
  font-weight: 600;
}
</style>
