<template>
  <header>
    <div class="head">
      <h3>
        {{ title }}
      </h3>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header",

  data() {
    return {
      title: "Header",
    };
  },
};
</script>

<style scoped>
header {
  background-color: rgb(219, 228, 209);
  padding: 8px;
  height: 50px;
  text-align: center;

  color: black;
  position: relative;
  bottom: 5px;
  width: 100%;
  /* opacity: .5; */
}
</style>
