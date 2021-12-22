<template>
  <div id="app">
    <Header />
    <DiskContainer />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import DiskContainer from "./components/DiskContainer.vue";
export default {
  name: "App",
  components: {
    Header, DiskContainer ,
  },
};
</script>

<style lang="scss">
@import url('./style/general.scss');
#app {
  width:100%;
  margin: auto;
  background-color: #1e2d3b;
  min-height: 100vh;
}
</style>
