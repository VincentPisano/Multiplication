<template>
  <div>
    <br />
    <h3>les tables de multiplications</h3>

    <button v-on:click="counter= 10">10 tables de multiplications</button>
    <button v-on:click="counter= 13">13 tables de multiplications</button>
    <div v-for="k in counter" v-bind:key="k">
      <les-table-multiplication v-bind:n="k"></les-table-multiplication>
    </div>
    <hr />
  </div>
</template>

<script>
import lesTableMultiplication from "../components/TableMultiplication.vue";
export default {
  name: "home",
  data: function() {
    return {
      n: 8,
      counter: 10
    };
  },
  components: {
    lesTableMultiplication
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.div{
  display:flex;
}
</style>