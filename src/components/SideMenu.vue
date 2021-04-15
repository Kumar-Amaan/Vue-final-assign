<template>
  <div class="menu">
  <button id="btn">SideMenu</button></div>
</template>

<script>
export default {
  name: "SideMenu",
};
</script>

<style scoped>
.menu {
  width: 100px;
  height: 37px;
  position: fixed;
  left: 1px;
  top: 50px;
  font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
  font-size: 20px;
  color: rgb(23, 31, 31);
  border: 2px solid;
  padding: 10px;
  box-shadow: 5px 10px;
}
</style>
