<template>
  <p>{{ title }}</p>
  <input type="text" ref="name" />
  <button @click="handleClick">Click Me</button>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      title: "My First Vue App:",
    };
  },
  methods: {
    handleClick() {
      console.log(this.$refs.name);
      this.$refs.name.classList.add("active");
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
p {
  color: red;
}
</style>
