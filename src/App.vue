<template>
  <div>
    <Header /> 
    <Main />
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header-footer/Header";
import Footer from "./components/Header-footer/Footer";
import Main from "./components/Main";

export default {
  name: "App",
  components: {
    Header,
    Footer,
    Main,
  },
};
</script>

<style>
@import "./assets/css/style.css";
</style>
