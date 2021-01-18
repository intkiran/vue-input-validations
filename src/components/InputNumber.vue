<template>
  <div>
    <h3>Vuejs Input Number Validation example</h3>
    <input id="number" @keypress="validateNumber" />
  </div>
</template>

<script>
export default {
  name: "InputNumber",
  data() {
    return {};
  },

  methods: {
    validateNumber: event => {
      const char = String.fromCharCode(event.keyCode);
      if (!/[0-9]/.test(char)) {
        event.preventDefault();
      }
    }
  }
};
</script>

<style scoped></style>
