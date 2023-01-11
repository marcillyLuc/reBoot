<template>
  <div class="frame">
    <main id="Home">
      <h1>Hello,</h1>
      <h2>
        this is a sandbox to apply good practices with
        <span class="aqua">VueJS / NuxtJS</span> !
      </h2>
    </main>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
main {
  min-width: 100vw;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  background: #000;
}
h1 {
  font-size: 100pt;
  font-weight: 300;
}
h2 {
  font-size: 17pt;
}
@media screen and (max-width: 700px) {
  h1 {
    font-size: 70pt;
  }
  h2 {
    font-size: 14pt;
    text-align: center;
    line-height: 24pt;
  }
}
</style>
