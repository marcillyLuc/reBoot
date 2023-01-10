<template>
  <div class="frame">
    <main id="Identify">
      <h3>Identify</h3>
      <p>Type your informations and see the result</p>
      <span class="aqua">...</span>
      <form>
        <label>What is your firstname?</label>
        <input type="text" v-model="firstName" />
        <label>What is your lastname?</label>
        <input type="text" v-model="lastName" />
        <label>Do you have a middlename?</label>
        <input type="text" v-model="middleName" />
        <label>How old are you?</label>
        <input type="number" v-model.number="age" />
      </form>
      <div class="result">
        <p>
          Your full name is ...
          <span class="aqua">
            {{ fullname }}
          </span>
        </p>
        <p>
          You are <span class="aqua"> {{ age }}</span> years old.
        </p>
      </div>
    </main>
  </div>
</template>

<script>
export default {
  data() {
    return {
      firstName: "",
      lastName: "",
      middleName: "",
      age: 10,
    };
  },
  computed: {
    fullname() {
      return `${this.firstName} ${this.middleName} ${this.lastName}`;
    },
  },
};
</script>

<style scoped>
form {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 17pt 0;
}
label {
  margin: 7pt;
}
input {
  background-color: #222;
  padding: 4pt;
  margin: 7pt;
}
.result {
  font-size: 14pt;
}
@media screen and (max-width: 700px) {
  .result {
    font-size: 11pt;
  }
}
</style>
