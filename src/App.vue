<template>
  Hello Vue

  <AppButton @update="getUpdade">
    Save

    <template #icon>Icon </template>
  </AppButton>
</template>

<script>
import AppButton from "./components/AppButton.vue";
export default {
  name: "App",
  components: { AppButton },
  setup() {
    const getUpdade = (data) => {
      console.log("getUpdade", data);
    };
    return {
      getUpdade,
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
