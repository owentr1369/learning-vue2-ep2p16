<template>
  <div>
    <p>App</p>
    <a v-bind:href="linkVal"> Link </a>
    <button @click="changeLink">Click to change link</button>
  </div>
</template>

<script>
// Tat ca du lieu truyen qua html o dang du lieu tho
// computed thuc hien nhu mot function nhung chi duoc coi la 1 t
export default {
  name: "App",
  data() {
    return {
      linkVal: "https://www.google.com",
    };
  },
  methods: {
    changeLink: function () {
      this.linkVal = "https://www.facebook.com";
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
</style>
