<template>
  <div class="frame">
    <main id="Square">
      <h3>Square</h3>
      <p>
        Modify the square bellow
        <span class="aqua">...</span>
      </p>
      <section>
        <label>
          Change frame color
          <input type="checkbox" v-model="isAqua" />
        </label>
        <label
          >Choose a text color
          <select v-model="textColor">
            <option value="">White</option>
            <option value="text-aqua">Aqua</option>
          </select>
        </label>
        <label
          >Modify the size
          <input type="number" step="10" min="100" max="170" v-model="size" />
        </label>
        <div
          class="square"
          :class="[textColor, square_class]"
          :style="[
            {
              width: size + 'pt',
              height: size + 'pt',
              lineHeight: size + 'pt',
            },
          ]"
        >
          Hi !
        </div>
      </section>
    </main>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isAqua: false,
      textColor: "",
      size: 100,
    };
  },
  computed: {
    square_class() {
      return { isAqua: this.isAqua };
    },
  },
};
</script>

<style scoped>
section {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 17pt 0;
}
select,
input {
  background-color: #222;
  color: white;
  padding: 4pt;
  margin: 7pt;
  border: none;
  max-width: 70pt;
}
.square {
  width: 100pt;
  height: 100pt;
  background-color: #222;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 17pt;
  margin: 17pt 0;
  border: solid 7pt white;
  border-bottom-width: 17pt;
}
.isAqua {
  border-color: aqua;
}
.text-aqua {
  color: aqua;
}
</style>
