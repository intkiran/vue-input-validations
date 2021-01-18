<template>
  <div id="app">
    <InputNumber />
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import InputNumberError from "./components/InputNumberError.vue";

export default {
  name: "App",
  components: {
    HelloWorld,
    InputNumberError
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
