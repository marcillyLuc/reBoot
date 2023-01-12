<template>
  <div class="frame">
    <main id="Message">
      <h3>Message</h3>
      <p>
        Type a message and click the button
        <span class="aqua">...</span>
      </p>
      <section>
        <button @click="move">Move to bottom</button>
      </section>
      <article class="card" v-for="person in people" :key="person.name">
        <h4>{{ person.name }}</h4>
        <p class="message">{{ person.message }}</p>
        <input type="text" />
      </article>
    </main>
  </div>
</template>

<script>
export default {
  data() {
    return {
      people: [
        {
          name: "John",
          message: "Hello World",
        },
        {
          name: "Boris",
          message: "I love this website !",
        },
        {
          name: "Arthur",
          message: "My name is Arthur",
        },
      ],
    };
  },
  methods: {
    move() {
      const first = this.people.shift();
      this.people.push(first);
    },
  },
};
</script>

<style scoped>
.card {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 10pt;
  margin: 17pt 0;
  background-color: #222;
  border: solid 1pt #333;
}
button {
  background: #333;
  padding: 10pt;
  border: solid 1pt #444;
}
.message {
  margin: 10pt 0;
  color: aqua;
}
input {
  background-color: #333;
  padding: 4pt;
  margin: 7pt;
  border: solid 1pt #444;
}
</style>
