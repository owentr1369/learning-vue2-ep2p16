<template>
  <div>
    <div
      class="vuong"
      @click="quanlido = !quanlydo"
      :class="{ do: quanlido }"
    ></div>
    <div
      class="vuong"
      @click="quanlido = !quanlydo"
      :class="{ do: quanlido }"
    ></div>
    <div class="vuong" :class="[color, { do: quanlido }]"></div>
    <div class="vuong"></div>
    <hr />
    <input type="text" v-model="color" />
  </div>
</template>

<script>
// Tat ca du lieu truyen qua html o dang du lieu tho
// computed thuc hien nhu mot function nhung chi duoc coi la 1 t
export default {
  name: "App",
  data() {
    return {
      quanlido: false,
      color: "xanhla",
    };
  },
  methods: {},
  computed: {
    divClasses: function () {
      return {
        do: this.quanlido,
        xanhduong: !this.quanlido,
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
.do {
  background-color: red;
}
.xanhduong {
  background-color: blue;
}
.xanhla {
  background-color: green;
}
</style>
