<template>
  <div class="hello">
    <h3>Vuejs Input type number validation</h3>
    <br />

    <input type="number" placeholder="Enter Number" v-model="mynumber"  @input="change($event)"
      @change="change($event)"/>
    <div class="error" v-if="!isValid">Number is Invalid</div
  </div>
</template>

<script>
export default {
  name: "InputNumberError",
  data() {
    return {
      mynumber: "",
      isValid: false,
      regex: /[0-9]/
    };
  },
  methods: {
    change:function(e){
      const number = e.target.value
      this.isNumberValid(url);
    },
    isNumberValid: function(inputNumber) {
      this.isValid=   this.regex.test(inputNumber)
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
.error{
  color:red;
}
</style>
