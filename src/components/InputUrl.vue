<template>
  <div class="hello">
    <h3>Vuejs Input type url validation</h3>
    <br />
  

    <input type="url" placeholder="Website url" v-model="email"  @input="change($event)"
      @change="change($event)"/>
    <div class="error" v-if="!isValid">URL is Invalid</div
  </div>
</template>

<script>
export default {
  name: "InputUrl",
  data() {
    return {
      url: "",
      isValid: false,
      regex: /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/
    };
  },
  methods: {
    change:function(e){
      const url = e.target.value
      this.isURLValid(url);
    },
    isURLValid: function(inputUrl) {
      this.isValid=   this.regex.test(inputUrl)
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
