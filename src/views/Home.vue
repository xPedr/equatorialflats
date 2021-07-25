<template>
  <div class="home">
    <h1>Amazing new flats in Brazil's zone equatorial</h1>
    <div class="block1">
      <img src="../assets/banners/sala-cozinha.jpg" alt="banner" id="img1" />
      <div id="txt1">
        <h2>Always warm!</h2>
        <p>
          On zone equatorial you can usufrute the Sun all year! Our products are placed in
          seaside cities! We have beach houses too!
        </p>
        <h3>Enjoy the heat when the summer never ends!</h3>
        <p>
          The flats are well placed and next to facilities like: shoppings, markets,
          schools, hospitals and much more!
        </p>
      </div>
    </div>
    <div class="block2">
      <div id="txt2">
        <h2>A complete investing</h2>
        <p>
          Our team will provide a complete service to your new flat. All our flats are
          mobiliated and new. The service provides access to amazing real estate options
          by accredited realtors, and constructors, and even the service of decoration.
        </p>
        <h4>
          Maybe you can think it costs a lot to have an apartment, or house, on Brazil
          zone equatorial ... but our basic services fee USD$50,000!!!
        </h4>
      </div>
      <img src="../assets/banners/sala-azul.jpg" alt="banner" id="img2" />
    </div>
    <img src="../assets/banners/sala-basica.jpg" alt="banner" id="img3" />
  </div>
</template>

<script>
export default {
  name: "Home",
};
</script>

<style scoped>
.home {
  padding-top: 40px;
  background: #f7ffde;
  border-radius: 10px;
  text-align: center;
}

.block1 {
  display: flex;
  flex-direction: row;
  padding: 30px 40px;
  align-items: center;
  justify-content: center;
}

.block1 img {
  margin: 0px 30px;
  border: 8px solid orange;
  border-radius: 15px;
}

#img1 {
  height: 500px;
}

#txt1 {
  width: 400px;
}

.block2 {
  display: flex;
  flex-direction: row;
  padding: 30px 40px;
  align-items: center;
  justify-content: center;
}

.block2 img {
  margin: 0px 30px;
  border: 8px solid orange;
  border-radius: 15px;
}

#img2 {
  height: 450px;
}

#txt2 {
  width: 400px;
}

#img3 {
  border: 12px solid white;
  border-radius: 40px;
}

@media (max-width: 700px) {
  .block1,
  .block2 {
    flex-direction: column;
  }

  #img1,
  #img2,
  #img3 {
    width: 400px;
    height: 350px;
  }
}
</style>
