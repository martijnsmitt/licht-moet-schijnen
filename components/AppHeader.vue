<template>
  <div class="header">
    <img
      src="~/assets/lichtmoetschijnen-logo.png"
      alt="Licht moet schijnen."
      class="header-logo"
    >
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.header {
  align-items: center;
  background: #b9a455;
  display: flex;
  height: 35vh;
  justify-content: center;
  max-height: 400px;
  min-height: 200px;
  position: relative;

  &-logo {
    height: 15vh;
    min-height: 150px;
  }
}
</style>
