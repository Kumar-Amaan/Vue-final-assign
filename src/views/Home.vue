<template>
  <div class="home">
    <Header name="Home" />
    <Footer name="Home" />
    <SideMenu name="Home" />
    <ApiCall name="Home" />
    
    <!-- <img alt="Vue logo" src="../assets/logo.png" /> -->
  </div>

</template>

<script>
// @ is an alias to /src
import Header from "../components/Header";
import Footer from "../components/Footer";
import SideMenu from "../components/SideMenu";
import ApiCall from '../components/ApiCall';

export default {
  name: "Home",
  components: {
    Header,
    Footer,
    SideMenu,
    ApiCall,
    
  },
};
</script>
