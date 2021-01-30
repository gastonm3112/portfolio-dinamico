<template>
  <Header />

  <Container />
</template>

<script>
import Container from "./components/Container";
import Header from "./components/Header";
export default {
  components: {
    Header,
    Container,
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
