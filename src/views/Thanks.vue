<template>
  <div id="thanks">
    <h1>Thank you for your contact</h1>
    <h4>INORI CONSULTANCE was mailed successful!</h4>
    <img src="../assets/author.jpg" alt="Pedro's photo" />
    <p>
      Hello! I'm Pedro Lima, and I will help you on this acquisition! The service I
      provide is a full access to purchase a real estate on a brazilian coastal city and
      interior design to the flat. You've sended me an form wich I'll read soon. Soon as
      possible I will return you a message to we start to discuss what you demand to our
      project. I work with discreet flats, and I am gladful you've contacted my services.
      Thank you for your consideration.
    </p>
  </div>
</template>

<script>
export default {
  name: "Thanks",
};
</script>

<style scoped>
#thanks {
  display: flex;
  flex-direction: column;
  width: 500px;
  background: #bdb759;
  margin: 15px auto;
  align-items: center;
  padding: 20px 40px;
}

#thanks img {
  height: 150px;
  border: 10px solid #1a3b1f;
  border-radius: 5rem;
}

#thanks p {
  font-size: 13px;
}

#thanks h1,
h4,
p {
  color: #1a3b1f;
}

@media (max-width: 600px) {
  #thanks {
    width: 370px;
  }
}
</style>
