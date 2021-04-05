<template>
  <div class="home">
    <h1>Todo App</h1>
    <Navbar />
    <router-view />
  </div>
</template>

<script>
import Navbar from "./components/Navbar";
export default {
  components: { Navbar },
};
</script>

<style lang="scss">
body {
  margin: 0;
  padding: 0;
}
.home {
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
h1 {
  text-align: center;
  font-size: 24px;
  font-weight: bold;
  margin-top: 10px;
}
</style>
