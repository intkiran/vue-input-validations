<template>
  <div id="app">
    <InputUrl />
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import InputUrl from "./components/InputUrl.vue";

export default {
  name: "App",
  components: {
    HelloWorld,
    InputUrl
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
