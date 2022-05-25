<template>
  <div>
    <div class="vuong" :style="{ backgroundColor: color }"></div>
    <div class="vuong" :style="customStyle"></div>
    <div class="vuong"></div>
    <div class="vuong"></div>
    <hr />
    <input type="text" v-model="color" />
    <input type="text" v-model="width" />
    <input type="text" v-model="height" />
  </div>
</template>

<script>
// Tat ca du lieu truyen qua html o dang du lieu tho
// computed thuc hien nhu mot function nhung chi duoc coi la 1 t
export default {
  name: "App",
  data() {
    return {
      color: "gray",
      width: 100,
      height: 100,
    };
  },
  methods: {},
  computed: {
    customStyle: function () {
      return {
        backgroundColor: this.color,
        width: this.width + "px",
        height: this.height + "px",
      };
    },
  },
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
.vuong {
  width: 100px;
  height: 100px;
  background-color: gray;
  display: inline-block;
  margin: 10px;
}
</style>
