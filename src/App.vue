<template>
  <div id="app">
    <Header />

    <Container />

    <Footer />
  </div>
</template>

<script>
import Container from "./components/Container";
import Header from "./components/Header";
import Footer from "./components/Footer";
export default {
  components: {
    Header,
    Container,
    Footer,
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Roboto&display=swap");
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Roboto", sans-serif;
}
</style>
