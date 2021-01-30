<template>
  <div id="container" class="container">
    <h2>Proyectos</h2>
    <hr />
    <div class="cards">
      <Cards />
    </div>
  </div>
</template>

<script>
import Cards from "./Cards.vue";
export default {
  components: { Cards },
  mounted() {
    this.getProjects();
  },
  methods: {
    async getProjects() {
      const res = await fetch("https://api.github.com/users/gastonm3112");

      const data = await res.json();

      console.log(data);
    },
  },
};
</script>

<style scoped>
.container {
  overflow: hidden;
  border: 1px solid #eee;
  box-shadow: 1px 1px 4px rgba(0, 0, 0, 0.6);
  text-align: center;
}
</style>
