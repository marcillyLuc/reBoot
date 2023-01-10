<template>
  <div class="frame">
    <nav>
      <a href="#Home">Home</a>
      <a href="#Identify">Identify</a>
      <a href="#Square">Square</a>
      <a href="#Condition">Condition</a>
      <a href="#Message">Message</a>
    </nav>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
nav {
  width: 100vw;
  position: fixed;
  display: flex;
  justify-content: flex-end;
  align-items: center;
  padding: 14pt 7pt;
}
a {
  margin: 0 4pt;
  opacity: 0.4;
  transition: opacity 140ms ease-in-out;
  &:hover {
    opacity: 1;
  }
}
@media screen and (max-width: 700px) {
  a {
    font-size: 10pt;
  }
  nav {
    justify-content: center;
  }
}
</style>
