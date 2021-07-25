<template>
  <div id="nav">
    <router-link to="/">
      <img src="../assets/logo.png" alt="logo" id="logo"
    /></router-link>
    <div id="links">
      <router-link to="/">Home</router-link> |
      <router-link to="/contact">Contact</router-link>
    </div>
  </div>
</template>

<script>
export default {
  name: "Nav",
};
</script>

<style scoped>
#logo {
  height: 66px;
  width: 100px;
}

#links {
}

#nav {
  display: flex;
  height: 70px;
  background: #f7ffde;
  justify-content: space-between;
  padding: 30px;
  align-items: center;
  border-radius: 10px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
  padding: 0px 20px;
  text-decoration: none;
  color: #515151;
  background: #f7ffde;
  padding: 10px 10px;
  transition: 0.5s;
}

#links a {
  border-top: solid 3px #ffb912;
  font-size: 18px;
}

#nav a.router-link-exact-active {
  color: #ffb912;
}

#nav a:hover {
  color: #ffb912;
}
</style>
