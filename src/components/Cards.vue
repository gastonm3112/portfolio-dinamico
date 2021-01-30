<template>
  <div id="cards">
    <div class="cards p-2">
      <h3>{{ title }}</h3>
      <p>
        {{ description }}
      </p>
      <p><strong>Autor Proyecto</strong></p>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    title: String,
    description: String,
  },
};
</script>

<style scoped>
.cards {
  width: 250px;
  margin: 7px;
  border: 1px solid #eee;
  box-shadow: 1px 1px 4px rgba(0, 0, 0, 0.6);
  text-align: center;
}
</style>
