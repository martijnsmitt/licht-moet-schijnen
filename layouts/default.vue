<template>
  <div class="wrapper">
    <app-header />
    <main>
      <nuxt />
    </main>
    <app-footer />
  </div>
</template>

<script>
import AppFooter from "@/components/AppFooter";
import AppHeader from "@/components/AppHeader";

export default {
  components: {
    AppFooter,
    AppHeader
  }
};
</script>
<style style="scss" scoped>
.wrapper {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

main {
  align-items: center;
  display: flex;
  flex-grow: 1;
  justify-content: center;
  padding: 15px 20px 35px;
}
</style>

