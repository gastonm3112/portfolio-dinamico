<template>
  <div id="cards_section">
    <h2>Proyectos</h2>
    <div class="container mt-5">
      <Loading v-if="loading" />
      <div class="cards" v-for="project in projects" :key="project.id">
        <Cards
          :title="project.name"
          :description="project.description"
          :autor="project.owner.login"
          :url="project.html_url"
          :homepage="project.homepage"
        />
      </div>
    </div>
  </div>
</template>

<script>
import Cards from "./Cards.vue";
import Loading from "./Loading.vue";
export default {
  data() {
    return {
      projects: null,
      loading: false,
    };
  },
  components: { Cards, Loading },
  mounted() {
    this.getProjects();
  },
  methods: {
    async getProjects() {
      this.loading = true;
      const res = await fetch("https://api.github.com/users/gastonm3112/repos");

      const data = await res.json();
      // Tomando información de mis proyectos
      this.projects = data;
      this.loading = false;
      console.log(data);
    },
  },
};
</script>

<style scoped>
#cards_section {
  text-align: center;
  margin-top: 1em;
}
.container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  overflow: hidden;
  border: 1px solid #eee;
  box-shadow: 1px 1px 4px rgba(0, 0, 0, 0.6);
  text-align: center;
}
.cards {
  padding: 1em;
}
</style>
