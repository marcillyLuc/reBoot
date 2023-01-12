<template>
  <div class="frame">
    <main id="Condition">
      <h3>Condition</h3>
      <p>
        Find the right answer to the question bellow
        <span class="aqua">...</span>
      </p>
      <section>
        What is the capital of France?
        <select v-model="answer">
          <option value="1">Response A</option>
          <option value="4">Response B</option>
          <option value="7">Response C</option>
        </select>
        <div v-if="answer == 1" class="result">
          <p>The capital of France is Tokyo ...</p>
          <h4>Wrong !</h4>
          <div class="square square-red"></div>
        </div>
        <div v-else-if="answer == 4" class="result">
          <p>The capital of France is London ...</p>
          <h4>Wrong !</h4>
          <div class="square square-red"></div>
        </div>
        <div v-else class="result">
          <p>The capital of France is Paris ...</p>
          <h4>Right !</h4>
          <div class="square square-aqua"></div>
        </div>
      </section>
    </main>
  </div>
</template>

<script>
export default {
  data() {
    return {
      answer: 1,
    };
  },
};
</script>

<style lang="scss" scoped>
select {
  background-color: #222;
  color: white;
  padding: 4pt;
  margin: 17pt 0;
  border: none;
  width: 100pt;
}
.result {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}
h4 {
  margin: 14pt;
}
.square {
  width: 40pt;
  height: 40pt;
  margin: 17pt 0;
  &-red {
    background-color: crimson;
  }
  &-aqua {
    background-color: aqua;
  }
}
</style>
