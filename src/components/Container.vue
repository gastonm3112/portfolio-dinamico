<template>
  <div id="container" class="container mt-5">
    <!-- <h2>Proyectos</h2> -->
    <div class="cards" v-for="project in projects" :key="project.id">
      <Cards
        :title="project.name"
        :description="project.description"
        :autor="project.owner.login"
        :url="project.html_url"
      />
    </div>
  </div>
</template>

<script>
import Cards from "./Cards.vue";
export default {
  data() {
    return {
      projects: null,
    };
  },
  components: { Cards },
  mounted() {
    this.getProjects();
  },
  methods: {
    async getProjects() {
      const res = await fetch("https://api.github.com/users/gastonm3112/repos");

      const data = await res.json();
      // Tomando información de mis proyectos
      this.projects = data;
      console.log(data);
    },
  },
};
</script>

<style scoped>
.container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  overflow: hidden;
  border: 1px solid #eee;
  box-shadow: 1px 1px 4px rgba(0, 0, 0, 0.6);
  text-align: center;
}
</style>
