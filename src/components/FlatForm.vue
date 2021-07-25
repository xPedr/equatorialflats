<template>
  <div id="form">
    <form action="https://formsubmit.co/pedrobbo@gmail.com" method="POST" id="flat-form">
      <div class="input-container">
        <label for="name">Name:</label>
        <input
          type="text"
          id="name"
          name="name"
          v-model="name"
          placeholder="Insert your name"
          required
        />
      </div>
      <div class="input-container">
        <label for="name">E-mail:</label>
        <input
          type="email"
          id="email"
          name="email"
          v-model="email"
          placeholder="email@email.com"
          required
        />
      </div>
      <div class="input-container">
        <label for="name">How many dormrooms?</label>
        <select name="rooms" id="rooms" v-model="rooms">
          <option value="room">Select rooms quantity</option>
          <option v-for="room in dormrooms" :key="room.id" :value="room.format">
            {{ room.format }}
          </option>
        </select>
      </div>
      <div class="input-container">
        <label for="name">Real estate type:</label>
        <select name="type" id="type" v-model="rooms">
          <option value="">Select real estate type</option>
          <option v-for="type in types" :key="type.id" :value="type.format">
            {{ type.format }}
          </option>
        </select>
      </div>
      <div class="input-container">
        <label for="name">Parking spaces:</label>
        <select name="garage" id="garage" v-model="rooms">
          <option value="">Select spaces quantity</option>
          <option v-for="garage in garages" :key="garage.id" :value="garage.format">
            {{ garage.format }}
          </option>
        </select>
      </div>
      <div class="input-container">
        <label for="name">Wich decoration style?</label>
        <select name="decoration" id="decoration" v-model="rooms">
          <option value="">Select decoration style</option>
          <option
            v-for="decoration in decorations"
            :key="decoration.id"
            :value="decoration.format"
          >
            {{ decoration.format }}
          </option>
        </select>
      </div>
      <input
        type="hidden"
        name="_next"
        value="https://equatorialflats.netlify.app/thanks"
      />
      <input
        type="hidden"
        name="_subject"
        value="EquatorialFlats - Formulario Recebido"
      />
      <input type="text" name="_honey" style="display: none" />
      <div class="input-container">
        <input type="submit" class="submit-btn" value="Contact administration" />
      </div>
    </form>
  </div>
</template>

<script>
export default {
  name: "FlatForm",
  data() {
    return {
      name: null,
      email: null,
      dormrooms: null,
      types: null,
      garages: null,
      decorations: null,
      msg: null,
    };
  },
  methods: {
    async getForm() {
      const req = await fetch("https://equatorialflats.netlify.app:3000/schemes");
      const data = await req.json();

      this.dormrooms = data.dormrooms;
      this.types = data.types;
      this.garages = data.garages;
      this.decorations = data.decorations;
    },
  },
  mounted() {
    this.getForm();
  },
};
</script>

<style scoped>
#flat-form {
  max-width: 400px;
  margin: 20px auto;
  background: #f7ffde;
  padding: 40px;
}

.input-container {
  display: flex;
  flex-direction: column;
  margin-bottom: 20px;
}

label {
  font-weight: bold;
  margin-bottom: 15px;
  color: #222;
  padding: 5px 10px;
  border-left: 4px solid #fcba03;
}

input,
select {
  padding: 5px 10px;
  width: 300px;
}

.submit-btn {
  background-color: #222;
  color: #fcba03;
  font-weight: bold;
  border: 2px solid #222;
  padding: 10px;
  font-size: 16px;
  margin: 0 auto;
  cursor: pointer;
  transition: 0.5s;
}

.submit-btn:hover {
  background-color: transparent;
  color: #222;
}
</style>
