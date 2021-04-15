<template>
  <footer>
    <div class="foot">
      <footer>
        <p>{{ footerText }}</p>
      </footer>
    </div>
  </footer>
</template>

<script>
export default {
  name: "Footer",

  data() {
    return {
      footerText: "Copyright Singhal@ 2021",
    };
  },
};
</script>
<style scoped>
* {
  padding: 0;
  margin: 0;
}
p {
  color: rgb(137, 224, 49);
  text-indent: 3%;
  position: relative;
  top: 13px;
  font-size: 40px;
}
.foot {
  position: absolute;
  top: 87%;
  right: 2px;
  width: 100%;
}
.foot {
  width: 100%;
  height: 100px;
  background-color: rgb(54, 62, 177);
  animation-name: footers;
  animation-duration: 15s;
  /* animation-iteration-count: 2; */
}

@keyframes footers {
  0% {
    background-color: red;
  }
  /* 15%{background-color: rgb(14, 10, 10);} */
  25% {
    background-color: yellow;
  }
  50% {
    background-color: blue;
  }
  100% {
    background-color: green;
  }
}
</style>
