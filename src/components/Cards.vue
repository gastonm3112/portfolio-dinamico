<template>
  <div id="cards">
    <div class="cards p-3">
      <h3>{{ title }}</h3>
      <p>
        {{ description }}
      </p>
      <p>
        <strong> {{ autor }} </strong>
      </p>
      <buttons-url :url="url" />
      <buttons-url
        color="red"
        :url="homepage"
        v-if="homepage != null"
        title="Deploy"
      />
    </div>
  </div>
</template>

<script>
import ButtonsUrl from "./ButtonsUrl";
export default {
  components: { ButtonsUrl },
  props: {
    title: String,
    description: String,
    autor: String,
    url: String,
    homepage: String,
  },
};
</script>

<style scoped>
.cards {
  width: 300px;
  margin: 7px;
  border: 1px solid #eee;
  box-shadow: 1px 1px 4px rgba(0, 0, 0, 0.6);
  text-align: center;
}
</style>
