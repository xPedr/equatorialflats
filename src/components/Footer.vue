<template>
  <footer>
    <div id="footer">
      <div id="whatsapp">
        <a href=" http://api.whatsapp.com/send?phone=5585986473342"
          ><img src="../assets/whatsapp.png" alt="whatsapp"
        /></a>
        <h3>Contact by Whatsapp</h3>
      </div>
      <div id="message">
        <a href="mailto:pedrobbo@gmail.com"
          ><img src="../assets/message.png" alt="email"
        /></a>
        <h3>or contact by E-mail</h3>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "Footer",
};
</script>

<style scoped>
footer {
  height: 100px;
  background: #f7ffde;
  border-radius: 10px;
}

div {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  margin: 0px 20px;
}

div img {
  height: 100px;
}

#whatsapp img,
#message img {
  padding: 0px 30px;
}

@media (max-width: 600px) {
  div {
    margin: 0;
  }
  #whatsapp img,
  #message img {
    padding: 0;
  }
}
</style>
