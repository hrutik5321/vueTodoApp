<template>
  <div class="navbar">
    <router-link class="left" to="/">Todo List</router-link>
    <router-link class="right" to="/about">About Us</router-link>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.navbar {
  height: 50px;
  width: 100%;
  background-color: #daff7d;
  margin-top: 25px;
  display: flex;
  font-size: 18px;
  font-weight: bold;
}
.left {
  width: 50%;
  height: 100%;
  text-align: center;
  display: flex;
  align-items: center;
  justify-content: center;
  border-right: 1px solid black;
  text-decoration: none;
}
.right {
  width: 50%;
  height: 100%;
  text-align: center;
  display: flex;
  align-items: center;
  justify-content: center;
  text-decoration: none;
}
</style>
